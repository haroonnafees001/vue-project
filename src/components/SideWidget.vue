<template>
  <div>
    <div v-for="(data,i) in obj" :key="i">
      <div class="card-header">
        <div class="card-title">
          <h1 class="title">{{data.title}}</h1>
        </div>
      </div>
      <div class="card-body">
        <ul>
          <li v-for="(val,i) in bodyData" class="mb-20" :key="i">
            <div class="media">
              <img class="mr-10" :src="val.img">
              <div class="media-body">
                <h5 class="mt-0">{{val.title}}</h5>
                <small class="text-gray">{{val.price}}</small>
              </div>
            </div>
          </li>

        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SideWidget",
  props: ['obj'],
  data: function () {
    return {
      bodyData:[]
    }
  },
  mounted() {
    this.getBodyData()
  },
  methods:{
    getBodyData:function (){
      this.obj.forEach((x) => {x.data.forEach((a) =>  this.bodyData.push(a) )});
    },
  }
}
</script>

<style scoped>

</style>