<template>
  <RouterView />
  <div>
    <div>
      <div class="hidden md:block">
      </div>
      <form data-test="formRegister">
        <h1 class="text-xl text-blue-700 font-bold">bienvenue</h1>
        <div>
          <InputText data-test="inputFirstname" :placeholder="'votre quartier'" />

          <InputText :placeholder="'votre ville'"/>

          <InputText data-test="inputLastname" :placeholder="'votre prenom'"/>
          <InputText data-test="inputLastname" :placeholder="'votre nom de famille'"/>
          <InputPassWord :placeholder="'mot de passe'" />
          <InputPassWord :placeholder="'confirmation mot de passe'"/>
          <InputDate :label="'date de naissance'"/>
        </div>

        <ButtonSubmit >register</ButtonSubmit>
      </form>
    </div>
  </div>
</template>


<script setup lang="ts">
import InputMail from './InputMail.vue';
import { helpers } from '@vuelidate/validators';
import { reactive, computed, ref } from 'vue';
import { useVuelidate } from '@vuelidate/core';
import { required, email, minLength, sameAs } from '@vuelidate/validators';
import { useI18n } from 'vue-i18n';
import { useRouter } from 'vue-router';
import InputText from "@/components/InputText.vue";
import ButtonSubmit from "@/components/ButtonSubmit.vue";
import InputPassWord from "@/components/InputPassWord.vue";
import InputDate from "@/components/InputDate.vue";
</script>
