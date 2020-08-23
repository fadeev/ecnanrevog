<template>
  <div>
    <app-layout>
      <app-text type="h1">ecnanrevog</app-text>
      <wallet />
      <type-list />
      <div @click="proposalSubmit">
        asd
      </div>
    </app-layout>
  </div>
</template>

<script>
export default {
  methods: {
    proposalSubmit() {
      const title = "t";
      const description = "d";
      const initial_deposit = [
        {
          denom: "stake",
          amount: "50",
        },
      ];
      this.$store.dispatch("txBroadcastGovProposal", {
        title,
        description,
        initial_deposit,
      });
    },
  },
};
</script>