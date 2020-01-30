<!--This is the initial view of our app-->
<template>
<!--always we need to define z-view as the main comp-->
  <z-view
  size="xxl">
    <!--iframe is an inline frame used to embed another document with the current html doc
      accelerometer is used in mobile phoneds to determine the phone's orientation
      gyroscope adds the additional dimension to the information supplied by the accelerometer-->
 <img src="croped.jpg" alt="Tensorflow">
    <div slot="extension">
      <!--we use slot.extension in this we can put several z-spots-->
      <!-- status monitor -->
      <div class="style1">
      <z-spot
        style="background-color:orange; border-width: 4px; border-color: var(--background-color);"
        :angle="315"
        size="m"
        :distance="130"
        to-view="Status">
        <!--toiView prop allow us to go to another view-->
        <i style="color: var( --accent-text-color)" class="fas fa-bell"></i><br>
        <span style="color: var( --accent-text-color)">6</span>
      </z-spot>
      <!-- location-->
      <z-spot :angle="190"
        size="m"
        :distance="130"
        label="Location"
        label-pos="left"
        to-view="location">
       <img slot="image" src="map.gif" width="100%" height="100%" style="opacity: 1">
      </z-spot>
      <!-- ClientCountryTimings-->
      <z-spot
        :angle="160"
        size="m"
        :distance="130"
        label="Client-Timings"
        label-pos="left"
        to-view="scenes">
       <img slot="image" src="digital.gif" width="100%" height="100%" style="opacity: 1">
      </z-spot>
      <!-- rooms-->
      <z-spot :angle="130"
        size="m"
        :distance="130"
        label="OfficeInterior"
        label-pos="left"
        to-view="rooms">
      <img slot="image" src="interior.gif" width="100%" height="100%" style="opacity: 1">
      </z-spot>
      <!-- Achievements-->
      <z-spot
        :angle="-135"
        :distance="130"
        size="m"
        label="Achievements"
        label-pos="left"
        to-view="devices">
        <img slot="image" src="faccenet.gif" width="100%" height="100%" style="opacity: 1">
      </z-spot>
      <!-- settings-->
      <z-spot
        :angle="90"
        :distance="131"
        size="m"
        label="Settings"
        label-pos="left"
        to-view="settings">
        <i class="fas fa-cog fa-spin" style="color:#0b35c2;"></i>
      </z-spot>
      <!--about us-->
      <z-spot
        :angle="-90"
        size="m"
        :distance="130"
        label="About us"
        label-pos="left"
        to-view="aboutus">
        <img slot="image" src="neuron.gif" width="100%" height="100%" style="opacity: 1">
      </z-spot>
      <!--<z-spot class="circle" style=' background-color: var(--shade-color);border-width: 3px;  border-color:white ;' size="xxs" :angle="-10"  :distance="150"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" size="xxs" :angle="-20" style=' background-color: var(--shade-color);border-width: 3px;  border-color:white ; ' :distance="150"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" size="xxs" :angle="-30" style=' background-color: var(--shade-color);border-width: 3px;  border-color:white ; ' :distance="150"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" size="xxs" :angle="-40" style=' background-color: var(--shade-color);border-width: 3px;  border-color:white ; ' :distance="150"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" size="xxs" :angle="-50" style=' background-color: var(--shade-color);border-width: 3px;  border-color:white ;' :distance="150"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance="150" :angle="-60"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance="150" :angle="-70"> <img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance="150" :angle="-80"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance="150" :angle="-90"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance=150 :angle="-100"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance=150 :angle="-110"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance=150 :angle="-120"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance=150 :angle="-130"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance=150 :angle="-140"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="-150"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width: 3px;  border-color:white;' size=xxs :distance=150 :angle="-160"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="-170"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="-180"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="-190"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="-200"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="-210"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="-220"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="-230"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="-240"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="10"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="20"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="30"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="40"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="50"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="60"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="70"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="80"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="90"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="100"><img slot="image" src="neuron.gif"></z-spot>
      <z-spot class="circle" style='background-color: var(--shade-color);border-width:3px;  border-color:white;' size=xxs :distance=150 :angle="110"><img slot="image" src="neuron.gif"></z-spot>-->
      </div>
     </div>
  </z-view>
</template>
<style>
.style1{
 color:#f5f3f1;
 
  }
  </style>
