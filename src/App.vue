<script>
export default {
  name: "App",
  data() {
    return {
      greet: "Hello",
      name: "Sanaz",
      location: "<b>Helsinki, Finland</b>",
      hack: `<a href='#' onclick='alert("You have been hacked!")'>Win a prize!</a>`,
      headingId: "heading",
      isDisabled: true,
      status: "danger",
      isPromoted: true,
      isSoldout: true,
      highlightColor: "orange",
      headerSize: 50,
      headerStyleObject: {
        color: "orange",
        fontSize: "50px",
        padding: "20px",
      },
      baseStyleObject: {
        fontSize: "50px",
        padding: "10px",
      },
      successStyleObject: {
        color: "green",
        backgroundColor: "lightgreen",
        border: "1px solid green",
      },
      dangerStyleObject: {
        color: "darkred",
        backgroundColor: "red",
        border: "1px solid darkred",
      },
    };
  },
};
</script>

<template>
  <p>{{ greet }} {{ name }}</p>
  <div v-html="location"></div>
  <div v-html="hack"></div>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 class="underline">Underlined Text</h2>
  <h2 class="underline" v-bind:class="status">Status</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 v-bind:class="isSoldout ? 'sold-out' : 'new'">Soldout? movie</h2>
  <h2 v-bind:class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">
    Array conditional movie
  </h2>
  <h2
    v-bind:class="{
      promoted: isPromoted,
      new: !isSoldout,
      'sold-out': isSoldout,
    }"
  >
    Object conditional movie
  </h2>
  <h2
    v-bind:style="{
      color: highlightColor,
      fontSize: headerSize + 'px',
      padding: '20px',
    }"
  >
    Inline Style
  </h2>
  <h2 v-bind:style="headerStyleObject">Object style</h2>
  <div v-bind:style="[baseStyleObject, successStyleObject]">Success Style</div>
  <div v-bind:style="[baseStyleObject, successStyleObject, dangerStyleObject]">
    Danger Style
  </div>
</template>

<style scoped>
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}

.new {
  color: olivedrab;
}

.sold-out {
  color: red;
}
</style>
