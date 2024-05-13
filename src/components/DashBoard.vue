<template>
  <div class="content">
    <h1 class="mb-20">Overview</h1>
    <div class="container">
      <div class="row">
        <div class="col-9">
              <Card  v-if="objCard" :obj="objCard"/>
              <GraphCard/>
              <TableCard v-if="objTable" :obj="objTable"/>
          </div>
        <div class="col-3">
          <div class="container">
            <div class="col-12" >
              <RightBar/>
            </div>
            </div>
          </div>
        </div>
      </div>
    </div>

</template>

<script>


import Card from './TheCard'
import GraphCard from './GraphCard'
import TableCard from "./TableCard";
import RightBar from "./RightBar";

export default {
  name: "DashBoard",
  components: {
    GraphCard,
    TableCard,
    Card,
    RightBar
  },
  data: function () {
    return {
       objCard : [
        {
          type:'card',
          title:'Document',
          icon:'description',
          description:'177.555',
          ratio:'10',

        },
        {
          type:'card',
          title:'Contact',
          icon:'phone_in_talk',
          description:'1400',
          ratio:'90',

        },
        {
          type:'card',
          title:'Email',
          icon:'mail',
          description:'170.555',
          ratio:'12',

        }
      ],
       objTable :[{
        type:'table',
        title:'Document',
        icon:'',
        description:'Document Tracking Information',
        data:[
          {
            name:'Annual Report',
            file:'PDF',
            category:'Property',
            author:'Diana',
            status:'Send',

          },
          {
            name:'Business Plan',
            file:'PDF',
            category:'Crypto',
            author:'James',
            status:'Send',

          },
          {
            name:'Marketing Tool',
            file:'Word',
            category:'Property',
            author:'Andy',
            status:'pending',

          }
        ]
      }],

    }
  },
}
</script>

<style scoped>

</style>