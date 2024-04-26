<script setup></script>

<template>
  <header>
    <div class="wrapper">
      <div>{{ greet }} {{ name }}</div>
      <div v-text="job"></div>
      <div v-html="channel"></div>
      <div v-html="hack"></div>
      <h3 v-bind:id="headingId">Attributes Binding</h3>
      <button v-bind:disabled="isDisabled">Bind</button>
      <h2 class="underline">Underlined text</h2>
      <h2 class="underline" v-bind:class="status">Status</h2>
      <h2 v-bind:class="isPromoted && 'promoted'">Promoted movie</h2>
      <h2 v-bind:class="isSolodout ? 'sold-out ' : 'new'">Soldout movies</h2>
      <p v-bind:class="['new', 'promoted']">newly promoted movies</p>
      <h3 v-bind:class="[isPromoted && 'promoted', isSolodout ? 'sold-out' : 'new']">
        Array approach binding class
      </h3>

      <h2
        v-bind:class="{
          promoted: isPromoted,
          new: !isSolodout,
          'sold-out': isSolodout
        }"
      >
        Object Conditional movie
      </h2>
    </div>
  </header>

  <RouterView />
</template>

<script>
export default {
  name: 'App',
  setup() {
    return {
      greet: 'Hello',
      name: 'Esther',
      job: 'developer',
      channel: '<h2> Code volution </h2>',
      hack: `<a href="#" onclick="alert('you have been hacked')">win price</a>`,
      headingId: 'headingId',
      isDisabled: true,
      status: 'success',
      isPromoted: true,
      isSolodout: false
    }
  }
}
</script>

<style>
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: green;
}

.sold-out {
  color: red;
}
</style>
