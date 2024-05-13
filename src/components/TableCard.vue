<template>
  <div class="container">
    <div v-for="(data,i) in obj" class="col-12" :key="i">
      <div class="card">
        <div class="card-header">
          <div class="card-title">
            <h1 class="title">
              {{ data.title }}
              <br>
              <b class="text-gray">{{ data.description }}</b>
            </h1>
            <select class="cselect">
              <option>Weekly</option>
              <option>Monthly</option>
              <option>Custom</option>
            </select>
          </div>
        </div>
        <div class="card-body">
          <div class="table-wrap">
            <table>
              <thead>
                <tr>
                  <th>Author</th>
                  <th>Category</th>
                  <th>File</th>
                  <th>Name</th>
                  <th>Status</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="(data,i) in tableData" :key="i">
                  <td>{{data.author}}</td>
                  <td>{{data.category}}</td>
                  <td>{{data.file}}</td>
                  <td>{{data.name}}</td>
                  <td>
                    <span class="tag tag-success" :class="{ 'tag-danger' : data.status.toLowerCase() === 'pending'}">
                      {{data.status}}
                    </span>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TableCard",
  props: ['obj'],
  data: function () {
    return {
      tableData:[]
    }
  },
  mounted() {
    this.getTableData()
  },
  methods:{
      getTableData:function (){
         this.obj.forEach((x) => {x.data.forEach((a) =>  this.tableData.push(a) )});
      },
  }

}
</script>

<style scoped>

</style>