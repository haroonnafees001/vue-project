<template>
  <div class="container">
    <div v-for="(data,i) in obj" class="col-4" :key="i">
      <div class="card">
        <div class="card-header">
          <div class="card-title">
            <h1 class="title"> {{ data.title }}</h1>
            <i class="icon">
              <span class="material-symbols-outlined">{{data.icon}}</span>
            </i>
          </div>
        </div>
        <div class="card-body">
          <div class="card-title">
            <h1 class="mt-20">{{data.description}}</h1>
          </div>
        </div>
        <div class="card-footer text-green font-size-12">
          <span class="mr-5 material-symbols-outlined ">trending_up</span>
          <span class="mr-5 ">{{data.ratio}} %</span>
          <span class="mr-5 text-gray">Since last week</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TheCard",
  props: ['obj'],
  data: function () {
    return {
    }
  },
  mounted() {
  },
  methods:{

  }

}
</script>

<style scoped>

</style>