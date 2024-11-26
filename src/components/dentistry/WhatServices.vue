<template>
  <!-- Main Heading -->
  <h1 class=" text-xl sm:text-2xl md:text-3xl lg:text-4xl text-center">
    {{ $t('dentistry.services.title')}}
  </h1>

  <!-- Main Content Area -->
  <div class="flex flex-col lg:flex-row  md:text-justify text-sm sm:text-base">
    <!-- Accordion Section -->
    <div class="w-full lg:w-1/2 p-4 sm:p-6 md:p-8">
      <p class="md:underline md:text-lg sm:text-xl md:text-center my-0 md:my-4 mb-8 md:mb-0 bg-customBeg md:bg-white p-6 md:p-0 rounded-2xl md:rounded-none">
        {{ $t('dentistry.services.sub-title')}}
      </p>
      <Accordion value="0">
        <AccordionPanel value="0">
          <AccordionHeader>{{ $t('dentistry.services.accordion.title-1')}} <div class="ml-20 bg-customPink p-2 rounded-2xl bg-opacity-40">> 250€</div></AccordionHeader>
          <AccordionContent>
            <p class="m-0">{{ $t('dentistry.services.accordion.text-1')}} </p>
          </AccordionContent>
        </AccordionPanel>
        <AccordionPanel value="1">
          <AccordionHeader>{{ $t('dentistry.services.accordion.title-2')}} <div class="bg-customPink p-2 rounded-2xl bg-opacity-40">140€</div></AccordionHeader>
          <AccordionContent>
            <p class="m-0">{{ $t('dentistry.services.accordion.text-2')}}</p>
          </AccordionContent>
        </AccordionPanel>
        <AccordionPanel value="2">
          <AccordionHeader>{{ $t('dentistry.services.accordion.title-3')}} <div class="bg-customPink p-2 rounded-2xl bg-opacity-40">250€</div></AccordionHeader>
          <AccordionContent>
            <p class="m-0">{{ $t('dentistry.services.accordion.text-3')}}</p>
          </AccordionContent>
        </AccordionPanel>
        <AccordionPanel value="3">
          <AccordionHeader>{{ $t('dentistry.services.accordion.title-4')}}</AccordionHeader>
          <AccordionContent>
            <p class="m-0">{{ $t('dentistry.services.accordion.text-4')}}</p>
          </AccordionContent>
        </AccordionPanel>
      </Accordion>
    </div>

    <!-- Description Section -->
    <div class="w-full lg:w-1/2 p-6 sm:p-6 md:p-8 flex bg-customDark text-white flex-col items-center justify-center space-y-4 md:rounded-2xl mt-8 lg:mt-0 lg:ml-8 ">
      <p>
        {{ $t('dentistry.services.text-1')}}
      </p>
      <p class="pt-6">{{ $t('dentistry.services.text-2')}}</p>
    </div>
  </div>
</template>

<script setup>
import Accordion from 'primevue/accordion';
import AccordionPanel from 'primevue/accordionpanel';
import AccordionHeader from 'primevue/accordionheader';
import AccordionContent from 'primevue/accordioncontent';
</script>
