<template>
  <!-- Main Heading -->
  <h1 class="mt-12 text-lg sm:text-xl md:text-2xl lg:text-3xl text-center">
    {{ $t('plastic.services.title')}}
  </h1>

  <!-- Main Content Area -->
  <div class="flex flex-col lg:flex-row text-justify text-sm sm:text-base">
    <!-- Accordion Section -->
    <div class="w-full lg:w-1/2 p-4 sm:p-6 md:p-8">
      <p class="md:underline md:text-lg sm:text-xl md:text-center my-0 md:my-4 mb-8 md:mb-0 bg-customBeg md:bg-white p-6 md:p-0 rounded-2xl md:rounded-none">
        {{ $t('plastic.services.sub-title')}}
      </p>
      <Accordion value="0">
        <AccordionPanel value="0" >
          <AccordionHeader>{{ $t('plastic.services.accordion.title-1')}} <div class=" bg-customPink p-2 rounded-2xl bg-opacity-40">3500€</div></AccordionHeader>
          <AccordionContent>
            <p class="m-0">
              {{ $t('plastic.services.accordion.text-1')}}
            </p>
          </AccordionContent>
        </AccordionPanel>
        <AccordionPanel value="1">
          <AccordionHeader>{{ $t('plastic.services.accordion.title-2')}} <div class="ml-6 bg-customPink p-2 rounded-2xl bg-opacity-40">3400€</div></AccordionHeader>
          <AccordionContent>
            <p class="m-0">
              {{ $t('plastic.services.accordion.text-2')}}
            </p>
          </AccordionContent>
        </AccordionPanel>
        <AccordionPanel value="2">
          <AccordionHeader>{{ $t('plastic.services.accordion.title-3')}} <div class="ml-8 bg-customPink p-2 rounded-2xl bg-opacity-40">2500€</div></AccordionHeader>
          <AccordionContent>
            <p class="m-0">
              {{ $t('plastic.services.accordion.text-3')}}
            </p>
          </AccordionContent>
        </AccordionPanel>
        <AccordionPanel value="3">
          <AccordionHeader>{{ $t('plastic.services.accordion.title-4')}} <div class="ml-12 bg-customPink p-2 rounded-2xl bg-opacity-40">> 2600€</div></AccordionHeader>
          <AccordionContent>
            <p class="m-0">
              {{ $t('plastic.services.accordion.text-4')}}
            </p>
          </AccordionContent>
        </AccordionPanel>
        <AccordionPanel value="4">
          <AccordionHeader>{{ $t('plastic.services.accordion.title-5')}} <div class=" bg-customPink p-2 rounded-2xl bg-opacity-40">>3200€</div></AccordionHeader>
          <AccordionContent>
            <p class="m-0">
              {{ $t('plastic.services.accordion.text-5')}}
            </p>
          </AccordionContent>
        </AccordionPanel>
      </Accordion>
    </div>

    <!-- Description Section -->
    <div
        class="w-full lg:w-1/2 p-8 md:p-12 flex bg-customDark text-white flex-col items-center justify-center space-y-4 rounded-2xl mt-8 lg:mt-0 lg:ml-8">
      {{ $t('plastic.services.text')}}

    </div>
  </div>
</template>

<script setup>
import Accordion from 'primevue/accordion';
import AccordionPanel from 'primevue/accordionpanel';
import AccordionHeader from 'primevue/accordionheader';
import AccordionContent from 'primevue/accordioncontent';
</script>
