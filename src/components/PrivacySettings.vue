<template>  <div>
    <h2 class="text-2xl mb-4">Privacy</h2>
    <form class="space-y-4 mx-auto" @submit.prevent="save">
      <div class="flex items-center gap-1">
        <input type="checkbox" v-model="privacy.searchEngineIndexing" />
        <label>Search engine indexing</label>
      </div>

      <div>
        <label class="mb-1">Visibility</label>
        <select v-model="privacy.visbility">
          <option value="private">Private</option>
          <option value="public">Public</option>
        </select>
      </div>

      <button type="submit" class="btn-primary">Save</button>
    </form>
  </div>
</template>

<script setup lang="ts">
import { useSettings } from '@/composables/useSettings';
import { useNotifications } from '@/composables/useNotifications.ts';

const { privacy } = useSettings();
const { addNotification } = useNotifications();
 
 const save = () => {
   addNotification(`Privacy settings were saved successfully`);
 }
</script>
