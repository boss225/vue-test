<template>
  <div style="width: 800px;">
    <div class="row mb-1">
      <div class="col-sm-2">begin</div>
      <div class="col-sm-10 pt-1">
        <div class="progress">
          <div
            role="progressbar"
            v-for="(item, index) in items"
            :key="index"
            aria-valuemin="0"
            aria-valuemax="100"
            aria-valuenow="66"
            class="progress-bar bg-success"
            :style="`background-color: ${item.color}; width:${item.size}`"  >
            {{item.title}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import jsonData from './JsonFiles/test3'
export default {
  name: 'Test3',
  data () {
    return {
      items: []
    }
  },
  mounted () {
    this.items = jsonData
  }
}
</script>

<style scoped>
  .mb-1, .my-1 {
    margin-bottom: 4px!important;
    margin-bottom: .25rem!important;
  }
  .row {
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    margin-right: -15px;
    margin-left: -15px;
  }
  .col-sm-2 {
     -ms-flex: 0 0 16.666667%;
     flex: 0 0 16.666667%;
     max-width: 16.666667%;
   }
  .col-sm-2, .col-sm-10 {
    position: relative;
    width: 100%;
    min-height: 1px;
    padding-right: 15px;
    padding-left: 15px;
  }
  .pt-1, .py-1 {
    padding-top: 4px!important;
    padding-top: .25rem!important;
  }
  .col-sm-10 {
    -ms-flex: 0 0 83.333333%;
    flex: 0 0 83.333333%;
    max-width: 83.333333%;
  }
  .progress, .progress-bar {
    display: -ms-flexbox;
    display: flex;
  }
  .progress {
    height: 16px;
    height: 1rem;
    overflow: hidden;
    font-size: 12px;
    font-size: .75rem;
    background-color: #e9ecef;
    border-radius: .25rem;
  }
  .progress-bar {
    -ms-flex-direction: column;
    flex-direction: column;
    -ms-flex-pack: center;
    justify-content: center;
    color: #fff;
    text-align: center;
    white-space: nowrap;
    background-color: #007bff;
    transition: width .6s ease;
  }
  .progress, .progress-bar {
    display: -ms-flexbox;
    display: flex;
  }
  * {
    -webkit-font-smoothing: antialiased;
  }
  *, :after, :before {
    box-sizing: border-box;
  }

</style>
