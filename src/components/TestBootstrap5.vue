<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string, src_link: string }>()

const count = ref(0)
</script>

<template>

  <div class="container">
    <div class="d-flex justify-content-between">
        <div></div>
        <div>
            <h4 class="text-muted">{{ msg }}</h4>
        </div>
        <div class="d-flex justify-content-end">
            <a :href="src_link" class="mr-1" target="_blank">Source</a>
        </div>
    </div>
</div>

<form class="container">
  <div class="form-floating pb-1">
        <textarea class="form-control" id="input" style="height: 150px"></textarea>
        <label for="input">Paste Input here</label>
    </div>
    <div>
        <button class="btn btn-info m-1">btn-info</button>

        <label class="form-check-label">
            <input class="form-check-input mx-2" type="checkbox" id="is_center" value="">form-check-label
        </label>
      </div>
      <div class="form-floating pt-1">
        <textarea class="form-control" id="output" style="height: 500px"></textarea>
        <label for="output">Result will be shown here</label>
      </div>
</form>
</template>
