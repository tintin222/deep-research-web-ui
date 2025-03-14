<script setup lang="ts">
  const { locale: globalLocale, t, setLocale } = useI18n()

  export type Locale = (typeof globalLocale)['value']
  export type AvailableLocales = Locale[]

  const props = defineProps<{
    /** Override display locale */
    value?: Locale
    /** If true, it will not change global locales */
    private?: boolean
  }>()

  const emit = defineEmits<{
    (e: 'update', value: Locale): void
  }>()

  // Only show English and Turkish in the dropdown
  const demoLocales = ['en', 'tr']
  
  const localeOptions = demoLocales.map((locale) => ({
    value: locale,
    label: t('language', {}, { locale }),
  }))

  function changeLocale(l: Locale) {
    emit('update', l)
    if (props.private) return
    setLocale(l)
  }
</script>

<template>
  <USelect
    icon="i-lucide-languages"
    :model-value="value ?? globalLocale"
    :items="localeOptions"
    @update:model-value="changeLocale($event)"
  />
</template> 