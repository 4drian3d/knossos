<template>
  <div class="normal-page">
    <div class="normal-page__sidebar">
      <aside class="universal-card">
        <h1>Legal</h1>
        <NavStack>
          <NavStackItem link="/legal/terms" label="Terms and Conditions">
            <HeartHandshakeIcon />
          </NavStackItem>
          <NavStackItem link="/legal/privacy" label="Privacy Policy">
            <LockIcon />
          </NavStackItem>
          <NavStackItem link="/legal/ccpa" label="California Privacy Notice">
            <InfoIcon />
          </NavStackItem>
          <NavStackItem link="/legal/rules" label="Content Rules">
            <ScaleIcon />
          </NavStackItem>
          <NavStackItem link="/legal/security" label="Security Notice">
            <ShieldIcon />
          </NavStackItem>
          <NavStackItem link="/legal/copyright" label="Copyright Policy">
            <CopyrightIcon />
          </NavStackItem>
          <NavStackItem link="/legal/cmp" label="Rewards Program Terms">
            <CurrencyIcon />
          </NavStackItem>
          <NavStackItem link="/legal/cmp-info" label="Rewards Program Info">
            <InfoIcon />
          </NavStackItem>
        </NavStack>
      </aside>
    </div>
    <div class="normal-page__content">
      <NuxtPage class="universal-card" :route="route" />
    </div>
  </div>
</template>

<script setup>
import {
  InfoIcon,
  HeartHandshakeIcon,
  LockIcon,
  ScaleIcon,
  ShieldIcon,
  CurrencyIcon,
  CopyrightIcon,
} from 'omorphia'
import NavStack from '~/components/ui/NavStack.vue'
import NavStackItem from '~/components/ui/NavStackItem.vue'

const route = useRoute()
</script>

<style lang="scss" scoped>
.normal-page__content :deep(a) {
  color: var(--color-link);
  text-decoration: underline;

  &:focus-visible,
  &:hover {
    color: var(--color-link-hover);
  }

  &:active {
    color: var(--color-link-active);
  }
}
</style>
