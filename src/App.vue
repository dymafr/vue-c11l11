<template>
  <form @submit="submit">
    <div>
      <label>Activités</label>
      <button type="button">Ajouter une activité</button>
    </div>
    <button>Envoi</button>
  </form>
</template>

<script setup lang="ts">
import { useFieldArray, useForm } from 'vee-validate';
import { z } from 'zod';
import { toFieldValidator } from '@vee-validate/zod';

const { handleSubmit, values } = useForm();

const submit = handleSubmit(() => {});

const { value: cityValue, errorMessage } = useFieldArray('address.city');
</script>

<style scoped lang="scss"></style>
