
<template>
    <div class="calendar-wrap">
        <div ref="cont" style="width: 100%; min-height: 100vh"></div>
    </div>
  </template>
   
  <script>
  import { Scheduler } from "dhtmlx-scheduler";
   
   
  export default {
    props: {
        events: {
            type: Array,
            default: []
        }
    },
    mounted() {
        let scheduler = Scheduler.getSchedulerInstance();
        var dateToStr = scheduler.date.date_to_str("%M %j");
        scheduler.templates.format_date = function(date){
            return dateToStr(date);
        };
        scheduler.config.header = {
            rows: [
                {
                    cols: [
                        
                        'spacer',
                        'month',
                        'week',
                        'day',
                        'agenda'
                    ]
                },
                {
                    cols: [
                        "today",    
                        "prev",
                        "next",
                        "date",
                    ]
                }
            ]
        }
        scheduler.config.start_on_monday = false;
        scheduler.config.default_date = "%l %M %j";
        scheduler.config.date_format = "%Y-%m-%d %H:%i";
        scheduler.config.day_date = "%D %d/%m";
        scheduler.config.hour_date = "%g:%i %A";
        scheduler.config.week_date = "%D";
        scheduler.config.month_date = "%F %Y";
        scheduler.config.month_day = "%j";
        scheduler.config.mark_now = true;
        
        scheduler.config.icons_select = [];
        scheduler.templates.event_header = function(start,end,ev){
            return ``;
        };
        scheduler.templates.event_date = function(date){
            return '';
        }
        scheduler.templates.week_date = function(start, end){
            return dateToStr(start) +" &ndash; "+ dateToStr(scheduler.date.add(end,-1,"day"));
        };
        const formatDayScale = scheduler.date.date_to_str("%D %d/%m");
 
        scheduler.templates.day_scale_date = function(date){
            return formatDayScale(date);
        };
        scheduler.templates.event_class = function(start, end, event) {
            return "blue";
        };
            
        scheduler.plugins({
            agenda_view: true
        });

        scheduler.attachEvent("onEventSave",function(id,ev){
			if (!ev.text) {
				scheduler.alert("event name must not be empty");
				return false;
			}
			if (ev.text.length > 30) {
				scheduler.alert("event name must has maximum 30 symbols");
				return false;
			}
			return true;
		});

        scheduler.form_blocks["my_input"]={
            render:function(sns){
                return "<div class='dhx_cal_lcolor' style='height:60px;'>" +
                    "Event background color&nbsp;<input name='color' type='color' value='#3b86ff'></div>";
            },
            set_value:function(node,value,ev){
                node.querySelector("[name='color']").value = value||"#3b86ff";
            },
            get_value:function(node,ev){
                return node.querySelector("[name='color']").value;
            },
            focus:function(node){
                var input = node.querySelector("[name='color']"); 
                input.select(); 
                input.focus(); 
            }
        };
        
        scheduler.locale.labels.section_description = "Details";
       
        scheduler.config.lightbox.sections=[    
            { name:"event name", type:"textarea", map_to:"text", focus:true},
            { name:"event time", type:"time", map_to:"time"}, 
            { name:"notes", type:"textarea", map_to:"notes"},
            { name:"color", map_to:"color", type:"my_input" , focus:true}
        ];
 
        


        scheduler.init(this.$refs.cont, new Date(), "month");
        scheduler.parse(this.events);
        this.scheduler = scheduler;
    },
    unmounted() {
        this.scheduler.destructor();
        this.$refs.cont.innerHTML = "";
    }
  };
  </script>
   
  <style lang="scss">
    @import "../../node_modules/dhtmlx-scheduler/codebase/dhtmlxscheduler.css";
    .calendar-wrap {
        background-color: #fff;
        padding: 1rem;
    }
    .dhx_cal_event_clear:before {
        display: none;
    }
    .dhx_cal_header {
        border-left: var(--dhx-scheduler-header-border);
    }
    .dhx_cal_data {
        border-left: var(--dhx-scheduler-default-border);
    }
    .blue {
        --dhx-scheduler-event-background: #3b86ff;
        border-radius: var(--dhx-scheduler-border-radius);
        background: var(--dhx-scheduler-event-background);
        color: var(--dhx-scheduler-event-color);
        padding: 2px var(--dhx-scheduler-base-module);
        border: var(--dhx-scheduler-event-border);
        font-size: var(--dhx-scheduler-event-text-font-size);
        line-height: var(--dhx-scheduler-event-text-line-height);
        font-weight: var(--dhx-scheduler-event-text-font-weight);
    }
    .dhx_cal_tab {
        &[data-tab="month"] {
            border-bottom-right-radius: 0;
            border-top-right-radius: 0;
            border-right: none;
            margin: 0;
        }
        &[data-tab="day"] {
            border-radius: 0;
            border-left: none;
            margin: 0;
        }
        &[data-tab="week"] {
            border-radius: 0;
        }
        &[data-tab="agenda"]{
            border-bottom-left-radius: 0;
            border-top-left-radius: 0;
            border-left: none;
            margin: 0;
        }
    }
    .dhx_cal_prev_button,
    .dhx_cal_next_button {
        --dhx-scheduler-base-colors-icons: var(--dhx-scheduler-btn-color);
        --dhx-scheduler-btn-background: var(--dhx-scheduler-btn-outline-background);
        --dhx-scheduler-btn-color: var(--dhx-scheduler-btn-outline-color);
        --dhx-scheduler-btn-border-color: var(--dhx-scheduler-btn-outline-border-color);
        --dhx-scheduler-btn-background-hover: var(--dhx-scheduler-btn-outline-background-hover);
        --dhx-scheduler-btn-color-hover: var(--dhx-scheduler-btn-outline-color-hover);
        --dhx-scheduler-btn-border-hover: var(--dhx-scheduler-btn-outline-border-hover);
        --dhx-scheduler-btn-background-active: var(--dhx-scheduler-btn-outline-background-active);
        --dhx-scheduler-btn-color-active: var(--dhx-scheduler-btn-outline-color-active);
        --dhx-scheduler-btn-border-active: var(--dhx-scheduler-btn-outline-border-active);
        --dhx-scheduler-btn-background-disabled: var(--dhx-scheduler-btn-outline-background-disabled);
        --dhx-scheduler-btn-color-disabled: var(--dhx-scheduler-btn-outline-color-disabled);
        --dhx-scheduler-btn-border-color-disabled: var(--dhx-scheduler-btn-outline-border-color-disabled);
        width: auto;
        background: var(--dhx-scheduler-btn-background);
        color: var(--dhx-scheduler-btn-color);
        border: 1px solid var(--dhx-scheduler-btn-border-color);
        border-radius: var(--dhx-scheduler-border-radius);
        height: var(--dhx-scheduler-control-height);
        padding: var(--dhx-scheduler-btn-padding, 0 20px);
        display: flex;
        justify-content: center;
        align-items: center;
        box-sizing: border-box;
        gap: 4px;
        flex-shrink: 0;
        font-weight: 500;
        font-size: var(--dhx-scheduler-font-size);
        font-family: var(--dhx-scheduler-font-family);
        font-weight: var(--dhx-scheduler-btn-font-weight, normal);
        line-height: 142%;
        text-transform: var(--dhx-scheduler-btn-text-transform);
        cursor: pointer;
        &:active {
            background: var(--dhx-scheduler-btn-background-active);
            color: var(--dhx-scheduler-btn-color-active);
            border-color: var(--dhx-scheduler-btn-border-active);
        }
        &:before {
            font-size: inherit;
            font-family: inherit !important;
            color: inherit;
        }
    }
    .dhx_cal_today_button {
        margin: 0;
        border-top-right-radius: 0;
        border-bottom-right-radius: 0;
        border-right: none;
    }
    .dhx_cal_prev_button {
        border-radius: 0;
    }
    .dhx_cal_next_button {
        border-top-left-radius: 0;
        border-bottom-left-radius: 0;
        border-left: none;
    }
    .dhx_cal_prev_button:before {
        content: "Back";
    }
    .dhx_cal_next_button:before {
        content: "Next";
    }
  </style>