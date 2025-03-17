<template>
    <section class="flow section" data-padding="compact">
      <div class="wrapper" id="main">
        <div class="invoice-actions">
  
          <Button @click="dialog1 = true">
            Show Dialog
          </Button>
  
          <!-- Dialog Component -->
          <Dialog v-model="dialog1" :options="dialogOptions"/>
        </div>
      </div>
    </section>
  </template>
  <script setup>
  import { ref } from "vue";
  import { Button, Dialog } from "frappe-ui";
  
  const dialog1 = ref(false);
  
  const createPromise = () => {
    return new Promise((resolve) => {
      setTimeout(() => {
        resolve();
        dialog1.value = false; // Close dialog after confirmation
      }, 1000);
    });
  };
  
  const dialogOptions = {
    title: "Confirm",
    message: "Are you sure you want to confirm this action?vhnvngdh Are you sure you want to confirm this action?vhnvngdhAre you sure you want to confirm this action?vhnvngdhAre you sure you want to confirm this action?vhnvngdhAre you sure you want to confirm this action?vhnvngdhAre you sure you want to confirm this action?vhnvngdh",
    size: "xl",
    icon: {
      name: "alert-triangle",
      appearance: "warning",
    },
    actions: [
      {
        label: "Confirm",
        variant: "solid",
        onClick: createPromise,
      },
    ],
  };
  </script>