<template>
    <RouterView />
    <div>
        <div>
            <div class="hidden md:block">
            </div>
            <form data-test="formRegister">
                <h1 class="text-xl text-blue-700 font-bold">{{ title }}</h1>
                <div>
                    <InputText data-test="inputLastname" :placeholder="'votre prenom'"/>
                    <InputText data-test="inputLastname" :placeholder="'votre nom de famille'"/>
                    <InputPassWord :placeholder="'mot de passe'" />
                    <InputPassWord :placeholder="'confirmation mot de passe'"/>
                </div>

                <ButtonSubmit >register</ButtonSubmit>
            </form>
        </div>
    </div>
</template>

<script setup lang="ts">
import InputText from "@/components/InputText.vue";
import ButtonSubmit from "@/components/ButtonSubmit.vue";
import InputPassWord from "@/components/InputPassWord.vue";

import { ref } from "vue";

const title = ref<string>("titre");
</script>