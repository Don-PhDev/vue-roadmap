<template>
  <div>
    <h3 :id="headingId">Heading</h3>
    <button :disabled="isDisabled">Click me</button>
    <h3 class="underline">Underlined text</h3>
    <h3 class="underline" :class="status">Status</h3>
    <h3 :class="isPromoted ? ['success', 'underline'] : 'danger' ">Promoted</h3>
    <h3 :class="[isPromoted ? 'underline' : '', isSoldOut ? 'danger' : 'success' ]">Array conditional</h3>
    <h3 :class="{
         promoted: isPromoted,
         new: !isSoldOut,
         'sold-out': isSoldOut
      }">Object conditional
    </h3>
    <h3 :style="{
      color: highlight,
      fontSize: headerSize + 'px'
    }">Inline Style
    </h3>
    <h3 :style="headerStyles">Object style</h3>
    <div :style="[baseStyle, successStyle]">Array style</div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      headingId: "heading",
      isDisabled: true,
      status: "danger",
      isPromoted: true,
      isSoldOut: false,
      highlight: "orange",
      headerSize: 50,
      headerStyles: {
        color: "orange",
        fontSize: "50px",
      },
      baseStyle: {
        fontSize: "50px",
        border: "1px solid yellow"
      },
      successStyle: {
        color: "yellowgreen",
        border: "1px solid black"
      }
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline {
  text-decoration: underline;
}

.danger {
  color: red
}

.success {
  color: green
}

.sold-out {
  color: white;
  background-color: blue;
  padding: 1rem 1rem;
}
</style>
