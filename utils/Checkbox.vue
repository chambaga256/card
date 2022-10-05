<script >
  

  const props = defineProps({
  value: {
    type: String,
    default: "",
  },
  label: {
    type: String,
    default: "",
  },
  checked: {
    type: Boolean,
    default: false,
  },
  id: {
    type: String,
    default: "",
  },
  disabled: {
    type: Boolean,
    default: false,
  },
});
 
const emit = defineEmits({
  onChange: {
    type: "change",
    default: () => {},
  },
});
const wrapperClass = computed(() => {
  const { checked } = props;
  return {
    "check-box": true,
    "check-box--checked": checked,
  };
});
const handleClick = () => {
  emit("onChange", props.id);
};
</script>


<script setup>
 
</script>

<template>
  <div
    :class="wrapperClass"
    tabindex="0"
    role="checkbox"
    :aria-checked="props.checked"
    @click="handleClick"
    
  >
  
    <span :class="iconClass">
      <Square v-if="!props.checked" />
     
      <CheckedSquare v-if="props.checked" />
      
    </span>
    <span
      :id="`label-${props.id}`"
      class="label"
    >
      {{ props.label }}
    </span>
  </div>
</template>
