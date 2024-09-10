<script>
import Scheduler from "@/components/SchedulerComponent.vue";
import { getData } from "./data";
 
export default {
  components: { Scheduler },
  data() {
    return {
      events: getData(),
    };
  },
};
</script>
 
<template>
  <div class="container-wrap">
    <aside class="aside">
      <div class="logo">
        <a href="/" class="logo-link">Impekable</a>
      </div>
      <nav class="nav">
        <ul class="nav-items">
          <li class="nav-item">
            <a href="#" class="nav-item-link">
              <svg width="64px" height="64px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path fill-rule="evenodd" clip-rule="evenodd" d="M21.4498 10.275L11.9998 3.1875L2.5498 10.275L2.9998 11.625H3.7498V20.25H20.2498V11.625H20.9998L21.4498 10.275ZM5.2498 18.75V10.125L11.9998 5.0625L18.7498 10.125V18.75H14.9999V14.3333L14.2499 13.5833H9.74988L8.99988 14.3333V18.75H5.2498ZM10.4999 18.75H13.4999V15.0833H10.4999V18.75Z" fill="#a5a4bf"></path> </g></svg>
              Home
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-item-link">
              <svg width="64px" height="64px" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" id="chart-colum" class="icon glyph" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><path d="M7,12v9a1,1,0,0,1-1,1H3a1,1,0,0,1-1-1V12a1,1,0,0,1,1-1H6A1,1,0,0,1,7,12ZM21,6H18a1,1,0,0,0-1,1V21a1,1,0,0,0,1,1h3a1,1,0,0,0,1-1V7A1,1,0,0,0,21,6ZM13.5,2h-3a1,1,0,0,0-1,1V21a1,1,0,0,0,1,1h3a1,1,0,0,0,1-1V3A1,1,0,0,0,13.5,2Z" fill="#a5a4bf"></path></g></svg>
              Dashboard
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-item-link">
              <svg width="64px" height="64px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path d="M3 8L8.44992 11.6333C9.73295 12.4886 10.3745 12.9163 11.0678 13.0825C11.6806 13.2293 12.3194 13.2293 12.9322 13.0825C13.6255 12.9163 14.2671 12.4886 15.5501 11.6333L21 8M6.2 19H17.8C18.9201 19 19.4802 19 19.908 18.782C20.2843 18.5903 20.5903 18.2843 20.782 17.908C21 17.4802 21 16.9201 21 15.8V8.2C21 7.0799 21 6.51984 20.782 6.09202C20.5903 5.71569 20.2843 5.40973 19.908 5.21799C19.4802 5 18.9201 5 17.8 5H6.2C5.0799 5 4.51984 5 4.09202 5.21799C3.71569 5.40973 3.40973 5.71569 3.21799 6.09202C3 6.51984 3 7.07989 3 8.2V15.8C3 16.9201 3 17.4802 3.21799 17.908C3.40973 18.2843 3.71569 18.5903 4.09202 18.782C4.51984 19 5.07989 19 6.2 19Z" stroke="#a5a4bf" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path> </g></svg>
              Inbox
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-item-link">
              <svg fill="#a5a4bf" width="64px" height="64px" viewBox="0 0 52 52" data-name="Layer 1" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <path d="M31.9,39.5h6A1.42,1.42,0,0,0,39.4,38V14a1.42,1.42,0,0,0-1.5-1.5h-6A1.42,1.42,0,0,0,30.4,14V38A1.42,1.42,0,0,0,31.9,39.5Z"></path> <path d="M45.4,39.5h3A1.42,1.42,0,0,0,49.9,38V14a1.42,1.42,0,0,0-1.5-1.5h-3A1.42,1.42,0,0,0,43.9,14V38A1.42,1.42,0,0,0,45.4,39.5Z"></path> <path d="M25,39.5h0A1.37,1.37,0,0,0,26.5,38V14A1.42,1.42,0,0,0,25,12.5h0A1.42,1.42,0,0,0,23.5,14V38A1.37,1.37,0,0,0,25,39.5Z"></path> <path d="M16.6,39.5H18A1.42,1.42,0,0,0,19.5,38V14A1.42,1.42,0,0,0,18,12.5H16.5A1.42,1.42,0,0,0,15,14V38A1.45,1.45,0,0,0,16.6,39.5Z"></path> <path d="M3.6,39.5h6A1.42,1.42,0,0,0,11.1,38V14a1.42,1.42,0,0,0-1.5-1.5h-6A1.42,1.42,0,0,0,2.1,14V38A1.47,1.47,0,0,0,3.6,39.5Z"></path> </g> </g></svg>
              Products
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-item-link">
              <svg fill="#a5a4bf" width="64px" height="64px" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><path d="M18,2H6A2,2,0,0,0,4,4V22l3-3,2,3,3-3,3,3,2-3,3,3V4A2,2,0,0,0,18,2ZM12,16H8a1,1,0,0,1,0-2h4a1,1,0,0,1,0,2Zm0-4H8a1,1,0,0,1,0-2h4a1,1,0,0,1,0,2Zm4,4H15a1,1,0,0,1,0-2h1a1,1,0,0,1,0,2Zm0-4H15a1,1,0,0,1,0-2h1a1,1,0,0,1,0,2Zm0-5H8A1,1,0,0,1,8,5h8a1,1,0,0,1,0,2Z"></path></g></svg>
              Invoices
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-item-link">
              <svg width="64px" height="64px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path d="M16 7C16 9.20914 14.2091 11 12 11C9.79086 11 8 9.20914 8 7C8 4.79086 9.79086 3 12 3C14.2091 3 16 4.79086 16 7Z" stroke="#a5a4bf" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path> <path d="M12 14C8.13401 14 5 17.134 5 21H19C19 17.134 15.866 14 12 14Z" stroke="#a5a4bf" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path> </g></svg>
              Customers
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-item-link">
              <svg fill="#a5a4bf" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="64px" height="64px" viewBox="0 0 100 100" enable-background="new 0 0 100 100" xml:space="preserve"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <path d="M94.974,17.838c-0.127-1.257-1.16-2.241-2.443-2.277v-0.007H39.624c-1.315,0-2.384,1.004-2.513,2.284h-0.026v13.139h22.342 c1.174,0,2.127,0.896,2.243,2.039h0.023v29.232h11.009l6.488,6.487c0.456,0.677,1.229,1.122,2.106,1.122 c1.402,0,2.538-1.136,2.538-2.537v-5.072h8.698V62.24c1.197-0.033,2.188-0.889,2.417-2.027H95V17.838H94.974z"></path> <path d="M54.44,35.964H7.204v0.006c-1.144,0.031-2.067,0.91-2.181,2.033H5v37.835h0.046c0.205,1.015,1.09,1.779,2.158,1.809v0.006 h7.765v4.529c0,1.25,1.015,2.265,2.266,2.265c0.783,0,1.474-0.398,1.88-1.002l5.792-5.792H54.44c1.096,0,2.011-0.78,2.22-1.815 h0.045V38.003h-0.023C56.568,36.859,55.614,35.964,54.44,35.964z"></path> </g> </g></svg>
              Chat Room</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-item-link active">
              <svg viewBox="0 0 600 600" version="1.1" id="svg9724" sodipodi:docname="calendar.svg" inkscape:version="1.2.2 (1:1.2.2+202212051550+b0a8486541)" width="64px" height="64px" xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape" xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd" xmlns="http://www.w3.org/2000/svg" xmlns:svg="http://www.w3.org/2000/svg" fill="#a5a4bf"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <defs id="defs9728"></defs> <sodipodi:namedview id="namedview9726" pagecolor="#ffffff" bordercolor="#666666" borderopacity="1.0" inkscape:showpageshadow="2" inkscape:pageopacity="0.0" inkscape:pagecheckerboard="0" inkscape:deskcolor="#d1d1d1" showgrid="true" inkscape:zoom="0.84118632" inkscape:cx="136.11729" inkscape:cy="439.26059" inkscape:window-width="1920" inkscape:window-height="1009" inkscape:window-x="0" inkscape:window-y="1080" inkscape:window-maximized="1" inkscape:current-layer="g10449" showguides="true"> <inkscape:grid type="xygrid" id="grid9972" originx="0" originy="0"></inkscape:grid> <sodipodi:guide position="-260,300" orientation="0,-1" id="guide383" inkscape:locked="false"></sodipodi:guide> <sodipodi:guide position="300,520" orientation="1,0" id="guide385" inkscape:locked="false"></sodipodi:guide> <sodipodi:guide position="240,520" orientation="0,-1" id="guide939" inkscape:locked="false"></sodipodi:guide> <sodipodi:guide position="220,80" orientation="0,-1" id="guide941" inkscape:locked="false"></sodipodi:guide> <sodipodi:guide position="335,335" orientation="0,-1" id="guide1236" inkscape:locked="false"></sodipodi:guide> </sodipodi:namedview> <g id="g10449" transform="matrix(0.95173205,0,0,0.95115787,13.901174,12.168794)" style="stroke-width:1.05103"> <g id="path10026" inkscape:transform-center-x="-0.59233046" inkscape:transform-center-y="-20.347403" transform="matrix(1.3807551,0,0,1.2700888,273.60014,263.99768)"></g> <g id="g11314" transform="matrix(1.5092301,0,0,1.3955555,36.774048,-9.4503933)" style="stroke-width:50.6951"></g> <path id="rect348" style="color:#a3a0fb;fill:#a3a0fb;stroke-linecap:round;stroke-linejoin:round;-inkscape-stroke:none;paint-order:stroke fill markers" d="M 143.0012 -12.781343 A 42.041302 42.041302 0 0 0 100.9582 29.260344 L 100.9582 61.459996 L 27.434765 61.459996 A 42.045506 42.045506 0 0 0 -14.606185 103.50168 L -14.606185 575.97476 A 42.045506 42.045506 0 0 0 27.434765 618.01645 L 573.78036 618.01645 A 42.045506 42.045506 0 0 0 615.82336 575.97476 L 615.82336 103.50168 A 42.045506 42.045506 0 0 0 573.78036 61.459996 L 500.25692 61.459996 L 500.25692 29.260344 A 42.041302 42.041302 0 0 0 458.21597 -12.781343 A 42.041302 42.041302 0 0 0 416.17297 29.260344 L 416.17297 61.459996 L 342.64954 61.459996 L 342.64954 29.260344 A 42.041302 42.041302 0 0 0 300.60859 -12.781343 A 42.041302 42.041302 0 0 0 258.56558 29.260344 L 258.56558 61.459996 L 185.04215 61.459996 L 185.04215 29.260344 A 42.041302 42.041302 0 0 0 143.0012 -12.781343 z M 69.475714 226.90186 L 531.73941 226.90186 L 531.73941 533.93307 L 69.475714 533.93307 L 69.475714 226.90186 z "></path> <path style="color:#a3a0fb;fill:#a3a0fb;stroke-linecap:round;stroke-linejoin:round;-inkscape-stroke:none;paint-order:stroke fill markers" d="m 389.92187,265.81641 a 10.511401,10.511401 0 0 0 -10.50976,10.51171 v 76.44727 a 10.511401,10.511401 0 0 0 10.50976,10.50977 h 94.5586 a 10.511401,10.511401 0 0 0 10.50976,-10.50977 v -76.44727 a 10.511401,10.511401 0 0 0 -10.50976,-10.51171 z m 10.51172,21.02148 h 73.53711 v 55.42578 h -73.53711 z" id="rect1123-6"></path> <path style="color:#a3a0fb;fill:#a3a0fb;stroke-linecap:round;stroke-linejoin:round;-inkscape-stroke:none;paint-order:stroke fill markers" d="m 253.33008,265.81641 c -5.80553,-1.8e-4 -10.51189,4.70618 -10.51172,10.51171 v 76.44727 c 9e-4,5.80477 4.70695,10.50995 10.51172,10.50977 h 94.55664 c 5.80477,1.8e-4 10.51082,-4.705 10.51172,-10.50977 v -76.44727 c 1.7e-4,-5.80553 -4.70619,-10.51189 -10.51172,-10.51171 z" id="rect1123-6-2" sodipodi:nodetypes="ccccccccc"></path> <path style="color:#a3a0fb;fill:#a3a0fb;stroke-width:1.05103;stroke-linecap:round;stroke-linejoin:round;-inkscape-stroke:none;paint-order:stroke fill markers" d="m 116.73786,264.38955 c -5.80553,-1.8e-4 -10.51189,4.70618 -10.51172,10.51171 v 76.44727 c 9e-4,5.80477 4.70695,10.50995 10.51172,10.50977 h 94.55664 c 5.80477,1.8e-4 10.51082,-4.705 10.51172,-10.50977 v -76.44727 c 1.7e-4,-5.80553 -4.70619,-10.51189 -10.51172,-10.51171 z" id="rect1123-6-2-9" sodipodi:nodetypes="ccccccccc"></path> <path style="color:#a3a0fb;fill:#a3a0fb;stroke-width:1.05103;stroke-linecap:round;stroke-linejoin:round;-inkscape-stroke:none;paint-order:stroke fill markers" d="m 253.33027,394.38567 c -5.80553,-1.8e-4 -10.51189,4.70618 -10.51172,10.51171 v 76.44727 c 9e-4,5.80477 4.70695,10.50995 10.51172,10.50977 h 94.55664 c 5.80477,1.8e-4 10.51082,-4.705 10.51172,-10.50977 v -76.44727 c 1.7e-4,-5.80553 -4.70619,-10.51189 -10.51172,-10.51171 z" id="rect1123-6-2-1" sodipodi:nodetypes="ccccccccc"></path> <path style="color:#a3a0fb;fill:#a3a0fb;stroke-width:1.05103;stroke-linecap:round;stroke-linejoin:round;-inkscape-stroke:none;paint-order:stroke fill markers" d="m 389.92267,395.80832 c -5.80553,-1.8e-4 -10.51189,4.70618 -10.51172,10.51171 v 76.44727 c 9e-4,5.80477 4.70695,10.50995 10.51172,10.50977 h 94.55664 c 5.80477,1.8e-4 10.51082,-4.705 10.51172,-10.50977 v -76.44727 c 1.7e-4,-5.80553 -4.70619,-10.51189 -10.51172,-10.51171 z" id="rect1123-6-2-1-7" sodipodi:nodetypes="ccccccccc"></path> <path style="color:#a3a0fb;fill:#a3a0fb;stroke-width:1.05103;stroke-linecap:round;stroke-linejoin:round;-inkscape-stroke:none;paint-order:stroke fill markers" d="m 116.73805,392.95881 c -5.80553,-1.8e-4 -10.51189,4.70618 -10.51172,10.51171 v 76.44727 c 9e-4,5.80477 4.70695,10.50995 10.51172,10.50977 h 94.55664 c 5.80477,1.8e-4 10.51082,-4.705 10.51172,-10.50977 v -76.44727 c 1.7e-4,-5.80553 -4.70619,-10.51189 -10.51172,-10.51171 z" id="rect1123-6-2-9-2" sodipodi:nodetypes="ccccccccc"></path> </g> </g></svg>
              Calendar
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-item-link">
              <svg fill="#a5a4bf" height="64px" width="64px" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 512 512" xml:space="preserve"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <g> <path d="M492.51,158.033C438.49,27.618,288.45-34.53,158.034,19.49C27.619,73.51-34.53,223.549,19.49,353.965 C73.51,484.382,223.551,546.53,353.965,492.509C484.381,438.49,546.53,288.45,492.51,158.033z M142.887,302.854l-92.548,38.334 c-23.486-56.703-21.72-117.672,0.096-170.336l92.506,38.317C130.942,238.136,129.97,271.668,142.887,302.854z M341.149,50.433 l-38.317,92.506c-28.965-11.997-62.499-12.97-93.685-0.053l-38.335-92.547C227.515,26.853,288.484,28.619,341.149,50.433z M170.852,461.566l38.317-92.506c28.965,11.998,62.499,12.97,93.685,0.053l38.335,92.547 C284.486,485.148,223.517,483.38,170.852,461.566z M290.075,338.265c-45.36,18.789-97.55-2.829-116.339-48.189 c-18.789-45.362,2.829-97.553,48.19-116.341c45.36-18.788,97.55,2.829,116.339,48.19 C357.053,267.285,335.436,319.476,290.075,338.265z M461.566,341.148L369.06,302.83c11.998-28.965,12.971-62.498,0.053-93.684 l92.547-38.335C485.148,227.514,483.38,288.482,461.566,341.148z"></path> </g> </g> </g></svg>
              Help Center
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-item-link">
              <svg width="64px" height="64px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path fill-rule="evenodd" clip-rule="evenodd" d="M14.2788 2.15224C13.9085 2 13.439 2 12.5 2C11.561 2 11.0915 2 10.7212 2.15224C10.2274 2.35523 9.83509 2.74458 9.63056 3.23463C9.53719 3.45834 9.50065 3.7185 9.48635 4.09799C9.46534 4.65568 9.17716 5.17189 8.69017 5.45093C8.20318 5.72996 7.60864 5.71954 7.11149 5.45876C6.77318 5.2813 6.52789 5.18262 6.28599 5.15102C5.75609 5.08178 5.22018 5.22429 4.79616 5.5472C4.47814 5.78938 4.24339 6.1929 3.7739 6.99993C3.30441 7.80697 3.06967 8.21048 3.01735 8.60491C2.94758 9.1308 3.09118 9.66266 3.41655 10.0835C3.56506 10.2756 3.77377 10.437 4.0977 10.639C4.57391 10.936 4.88032 11.4419 4.88029 12C4.88026 12.5581 4.57386 13.0639 4.0977 13.3608C3.77372 13.5629 3.56497 13.7244 3.41645 13.9165C3.09108 14.3373 2.94749 14.8691 3.01725 15.395C3.06957 15.7894 3.30432 16.193 3.7738 17C4.24329 17.807 4.47804 18.2106 4.79606 18.4527C5.22008 18.7756 5.75599 18.9181 6.28589 18.8489C6.52778 18.8173 6.77305 18.7186 7.11133 18.5412C7.60852 18.2804 8.2031 18.27 8.69012 18.549C9.17714 18.8281 9.46533 19.3443 9.48635 19.9021C9.50065 20.2815 9.53719 20.5417 9.63056 20.7654C9.83509 21.2554 10.2274 21.6448 10.7212 21.8478C11.0915 22 11.561 22 12.5 22C13.439 22 13.9085 22 14.2788 21.8478C14.7726 21.6448 15.1649 21.2554 15.3694 20.7654C15.4628 20.5417 15.4994 20.2815 15.5137 19.902C15.5347 19.3443 15.8228 18.8281 16.3098 18.549C16.7968 18.2699 17.3914 18.2804 17.8886 18.5412C18.2269 18.7186 18.4721 18.8172 18.714 18.8488C19.2439 18.9181 19.7798 18.7756 20.2038 18.4527C20.5219 18.2105 20.7566 17.807 21.2261 16.9999C21.6956 16.1929 21.9303 15.7894 21.9827 15.395C22.0524 14.8691 21.9088 14.3372 21.5835 13.9164C21.4349 13.7243 21.2262 13.5628 20.9022 13.3608C20.4261 13.0639 20.1197 12.558 20.1197 11.9999C20.1197 11.4418 20.4261 10.9361 20.9022 10.6392C21.2263 10.4371 21.435 10.2757 21.5836 10.0835C21.9089 9.66273 22.0525 9.13087 21.9828 8.60497C21.9304 8.21055 21.6957 7.80703 21.2262 7C20.7567 6.19297 20.522 5.78945 20.2039 5.54727C19.7799 5.22436 19.244 5.08185 18.7141 5.15109C18.4722 5.18269 18.2269 5.28136 17.8887 5.4588C17.3915 5.71959 16.7969 5.73002 16.3099 5.45096C15.8229 5.17191 15.5347 4.65566 15.5136 4.09794C15.4993 3.71848 15.4628 3.45833 15.3694 3.23463C15.1649 2.74458 14.7726 2.35523 14.2788 2.15224ZM12.5 15C14.1695 15 15.5228 13.6569 15.5228 12C15.5228 10.3431 14.1695 9 12.5 9C10.8305 9 9.47716 10.3431 9.47716 12C9.47716 13.6569 10.8305 15 12.5 15Z" fill="#a5a4bf"></path> </g></svg>
              Settings
            </a>
          </li>
        </ul>
      </nav>
    </aside>
    <header class="header">
      <div class="header-left">
        <div class="search">
          <form action="" method="" class="search-form">
            <button type="submit" class="search-form-button"></button>
            <input type="search" placeholder="Search transactions, invoices or help" class="search-form-input">
          </form>
        </div>
      </div>
      <div class="header-right">
        <div class="links">
          <ul class="links-items">
            <li class="links-item">
              <a href="#" class="links-item-link">
                <svg fill="#a5a4bf" height="64px" width="64px" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 512 512" xml:space="preserve"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <g> <path d="M492.51,158.033C438.49,27.618,288.45-34.53,158.034,19.49C27.619,73.51-34.53,223.549,19.49,353.965 C73.51,484.382,223.551,546.53,353.965,492.509C484.381,438.49,546.53,288.45,492.51,158.033z M142.887,302.854l-92.548,38.334 c-23.486-56.703-21.72-117.672,0.096-170.336l92.506,38.317C130.942,238.136,129.97,271.668,142.887,302.854z M341.149,50.433 l-38.317,92.506c-28.965-11.997-62.499-12.97-93.685-0.053l-38.335-92.547C227.515,26.853,288.484,28.619,341.149,50.433z M170.852,461.566l38.317-92.506c28.965,11.998,62.499,12.97,93.685,0.053l38.335,92.547 C284.486,485.148,223.517,483.38,170.852,461.566z M290.075,338.265c-45.36,18.789-97.55-2.829-116.339-48.189 c-18.789-45.362,2.829-97.553,48.19-116.341c45.36-18.788,97.55,2.829,116.339,48.19 C357.053,267.285,335.436,319.476,290.075,338.265z M461.566,341.148L369.06,302.83c11.998-28.965,12.971-62.498,0.053-93.684 l92.547-38.335C485.148,227.514,483.38,288.482,461.566,341.148z"></path> </g> </g> </g></svg>
              </a>
            </li>
            <li class="links-item">
              <a href="#" class="links-item-link">
                <svg fill="#a5a4bf" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="64px" height="64px" viewBox="0 0 100 100" enable-background="new 0 0 100 100" xml:space="preserve"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <path d="M94.974,17.838c-0.127-1.257-1.16-2.241-2.443-2.277v-0.007H39.624c-1.315,0-2.384,1.004-2.513,2.284h-0.026v13.139h22.342 c1.174,0,2.127,0.896,2.243,2.039h0.023v29.232h11.009l6.488,6.487c0.456,0.677,1.229,1.122,2.106,1.122 c1.402,0,2.538-1.136,2.538-2.537v-5.072h8.698V62.24c1.197-0.033,2.188-0.889,2.417-2.027H95V17.838H94.974z"></path> <path d="M54.44,35.964H7.204v0.006c-1.144,0.031-2.067,0.91-2.181,2.033H5v37.835h0.046c0.205,1.015,1.09,1.779,2.158,1.809v0.006 h7.765v4.529c0,1.25,1.015,2.265,2.266,2.265c0.783,0,1.474-0.398,1.88-1.002l5.792-5.792H54.44c1.096,0,2.011-0.78,2.22-1.815 h0.045V38.003h-0.023C56.568,36.859,55.614,35.964,54.44,35.964z"></path> </g> </g></svg>
              </a>
            </li>
            <li class="links-item">
              <a href="#" class="links-item-link">
                <svg fill="#a5a4bf" width="64px" height="64px" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><path d="M20,18H4l2-2V10a6,6,0,0,1,5-5.91V3a1,1,0,0,1,2,0V4.09a5.9,5.9,0,0,1,1.3.4A3.992,3.992,0,0,0,18,10v6Zm-8,4a2,2,0,0,0,2-2H10A2,2,0,0,0,12,22ZM18,4a2,2,0,1,0,2,2A2,2,0,0,0,18,4Z"></path></g></svg>
              </a>
            </li>
          </ul>
        </div>
        <div class="account">
          <a href="#" class="account-link">
            <span class="account-name">John Doe</span>
            <img src="./assets/icons/users-avatar-svgrepo-com.svg" class="account-photo" alt="John Doe" />
          </a>
        </div>
      </div>
      
    </header>
    <main class="main">
      <Scheduler :events="events" />
    </main>
  </div>
</template>