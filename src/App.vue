<template>
  <div id="app">
    <base-checkbox v-model="lovingVue"></base-checkbox>
    <base-input @focus.native="onFoucs"></base-input>
    <text-document :title.sync="title"></text-document>
    <sumbit-button>save</sumbit-button>
    <base-layout>
      <template #header>
        <h1>Here might be a page title</h1>
      </template>
      <p>A paragraph for the main content.</p>
      <p>And another one.</p>
      <template #footer>
        <p>Here's some contact info</p>
      </template>
    </base-layout>
    <current-user>
      <template #default="slotProps">
        {{ slotProps.user.firstName }}
      </template>
    </current-user>
  </div>
</template>

<script>
import baseCheckbox from "@/components/base-check";
import baseInput from "@/components/base-input";
import textDocument from "@/components/text-document";
import sumbitButton from "@/components/submit-button";
import baseLayout from "@/components/base-layout";
import currentUser from "@/components/current-user";
export default {
  data() {
    return {
      lovingVue: true,
      title: "父组件title",
      user: {
        lastName: "lastName",
        firstName: "firstName"
      }
    };
  },
  components: {
    baseCheckbox,
    baseInput,
    textDocument,
    sumbitButton,
    baseLayout,
    currentUser
  }
};
</script>
<style lang="less"></style>
