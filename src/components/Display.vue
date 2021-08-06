<template>
    <div class="container">
        <div class="container">
            <div class="row">
                <div class="col-sm-8">
                    <input class="form-control" type="text" placeholder="Add Event ToDo"  v-model="events" aria-label="default input example">
                </div>
                <div class="col-sm-4" style="background">
                    <button type="button" class="btn btn-info" v-on:click="addevent()">ADD</button>
                </div>
            </div>
        </div>
        <br><br>
        <div class="row">
            <div class="col-sm-7">
                <ul>
                    <div class="row" v-for="(event,index) in list" v-bind:key="index">
                        <div class="col-sm-10">
                            <li>{{event}}</li>
                        </div>
                        <div class="col-sm-2">
                            <button type="button" class="btn btn-info" id="delete" v-on:click="deleteevent(index)">X</button>
                        </div>
                    </div>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'Display',
  data () {
    return { events: null, list: [] }
  },
  methods:
    {
      addevent: function () {
        // this.list.push(this.content),
        // this.content = ''
        this.list.push(this.events)
      },
      deleteevent: function (index) {
        console.log(index)
        this.list.splice(index, index)
      }
    }

}
</script>
<style scoped>
#delete{
    margin-left: 50px;
}
.row{
    margin-bottom: 15px;
}
ul{
    list-style-type: none;
}
</style>
