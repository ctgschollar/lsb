<template>
    <el-form ref="form" :model="form" id="check_availability" action="https://hotels.cloudbeds.com/reservation/A9p5sR" method="post">
      <el-row>
        <el-col :span="8">
          <el-date-picker name="widget_date" v-model="form.startDate" type="date" placeholder="Pick a day"></el-date-picker>
        </el-col>
        <el-col :span="8">
          <el-date-picker name="widget_date_to" v-model="form.endDate" type="date" placeholder="Pick a day"></el-date-picker>
        </el-col>
        <el-col :span="8">
          <input type="hidden" value="Y-m-d" name="date_format">
          <button type="submit" @click="onSubmit">Check Availability</button>
        </el-col>
      </el-row>
    </el-form>
</template>

<script>

export default {
  name: 'Footer',
  data () {
    return {
      mobile: false,
      span: 12,
      form:  {
        widget_date: '',
        widget_date_to: '',
        date_format:'Y-m-d',
        bf_submit:'',
      },
    }
  },
  methods: {
    onSubmit () {
      console.log(this.form.startDate);
      this.$http.post('https://hotels.cloudbeds.com/booking/reservation/R43szk',
                      this.form,
                      { headers : {
                        'content-type':'application/x-www-form-urlencoded'}
                      }).then( function(response) {
                        location.href = 'https://hotels.cloudbeds.com/booking/reservation/R43szk';
                      });
    },
  },
  created: function (){
    if (window.mobilecheck()){
      this.msg = "On mobile";
      this.mobile = true;
      this.span = 24;
    }
    else{
      this.msg = "Not mobile"
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.el-container img {
  width:100%;
}

.el-row {
  height:auto;
}

el-col {
  background-size:contain;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
