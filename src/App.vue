<template>
  <form>
    <div>
      <label>Activités</label>
      <button @click="push()" type="button">Ajouter une activité</button>
    </div>
    <div :key="field.key" v-for="{ field, i } in fields">
      <Field :name="`hobbies[${i}]`" />
    </div>
    <pre>{{ values }}</pre>
  </form>
</template>

<script setup lang="ts">
import { useForm, useFieldArray, Field } from 'vee-validate';
import { z } from 'zod';
import { toFieldValidator } from '@vee-validate/zod';

const { values } = useForm();

const { fields, push } = useFieldArray('hobbies');
</script>

<style scoped lang="scss"></style>
