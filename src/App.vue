<script setup></script>

<template>
  <header>
    <div class="wrapper">
      <div>{{ greet }} {{ name }}</div>
      <div v-text="job"></div>
      <div v-html="channel"></div>
      <div v-html="hack"></div>
      <h3 :id="headingId">Attributes Binding</h3>
      <button :disabled="isDisabled">Bind</button>
      <h2 class="underline">Underlined text</h2>
      <h2 class="underline" :class="status">Status</h2>
      <h2 :class="isPromoted && 'promoted'">Promoted movie</h2>
      <h2 :class="isSolodout ? 'sold-out ' : 'new'">Soldout movies</h2>
      <p :class="['new', 'promoted']">newly promoted movies</p>
      <h3 :class="[isPromoted && 'promoted', isSolodout ? 'sold-out' : 'new']">
        Array approach binding class
      </h3>

      <h2
        :class="{
          promoted: isPromoted,
          new: !isSolodout,
          'sold-out': isSolodout
        }"
      >
        Object Conditional movie
      </h2>

      <h2 :style="{ color: highlightColor, 'font-size': headerSize + 'px', padding: '20px' }">
        Inline style binding
      </h2>

      <p :style="headerSytleObject">Systle object</p>

      <div :style="[baseStyleObject, successStyleObject]">Success sytle</div>

      <div :style="[baseStyleObject, dangerStyleObject]">danger style</div>
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
      isSolodout: false,
      highlightColor: 'orange',
      headerSize: 50,
      headerSytleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px'
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '20px'
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid black',
        padding: '20px'
      },
      dangerStyleObject: {
        color: 'darkred',
        backgroundColor: 'red',
        border: '1px solid darkred'
      }
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
