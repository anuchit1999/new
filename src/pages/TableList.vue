<template>
<div class="row">
    <div class="col-12">
      <card :title="table1.title">
        <div class="table-responsive">
          <base-table
            :data="table1.data"
            :columns="table1.columns"
            thead-classes="text-primary"
          >
          </base-table>
          <div class="button1">
            <b-button pill variant="primary" href="https://stackpython.pythonanywhere.com/export-csv/">Download CSV</b-button>
          </div>
        </div>
      </card>
    </div> 
      
      <!--
      <div>
        <li style="color:red" v-for="garbage in garbages" :key="garbage">Hello
          <p style="color:red">{{ garbage.kind }}</p>
          {{ garbage.count }}
        </li>
        <p style="color:red" v-if="errors"> This is error </p>
      </div> -->

  </div>



</template>
<script>
import axios from 'axios'  // Axios
/*
export default {
  data() {
    return {
      garbages: [],
      errors: true
    }
  },

  // Fetches posts when the component is created.
  created() {
    axios.get(`http://127.0.0.1:8000/api/garbages/`)
    .then(response => {
      // JSON responses are automatically parsed.
      this.garbages = response.data
      console.log(response.data)
    })
    .catch(e => {
      this.errors.push(e)
    })
  }
};
*/ 

import { BaseTable } from "@/components";
const tableColumns = ["No", "Kind", "Weight", "DateTime"];
const tableData = [
  
 
  {
     id:3,
    no: 1,
    kind: "Bottle",
    weight: 35.8,
    datetime: "2021-06-09, 08.03"
  },
  {
    id:2,
    no: 2,
    kind: "Bottle",
    weight: 35.9,
    datetime: "2021-06-08, 08.13"
  },
  {
    id:1,
    no: 3,
    kind: "Plastic",
    weight: 69.2,
    datetime: "2021-06-08, 08.03"
  },
];

export default {
  components: {
    BaseTable
  },
  data() {
    return {
      table1: {
        title: "Garbage Logs",
        columns: [...tableColumns],
        data: [...tableData]
      },
      table2: {
        title: "Table on Plain Background",
        columns: [...tableColumns],
        data: [...tableData]
      } 
    };
  }
}; 
</script>

<style>
.button1 {
  margin-top: 50px;
  text-align: center;
}
</style>
