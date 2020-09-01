<template>
  <div id="app">
    <div class="container">
      <form>
        <div class="form-group row">
          <label for="mail" class="col-sm-2 col-form-label">Email</label>
          <div class="col-sm-10">
            <input type="email" class="form-control" id="mail" placeholder="Email" v-model="user.mail">
          </div>
        </div>
        <div class="form-group row">
          <label for="Password" class="col-sm-2 col-form-label">Password</label>
          <div class="col-sm-10">
            <input type="password" class="form-control" id="Password" placeholder="Password" v-model="user.password">
          </div>
        </div>
        <fieldset class="form-group">
          <div class="row">
            <div class="col-sm-10">
              <div class="form-check">
                <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios1" value="Male" checked v-model="user.gender">
                <label class="form-check-label" for="gridRadios1">
                  Male
                </label>
              </div>
            </div>
              <div class="form-check">
                <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios2" value="Female" v-model="user.gender">
                <label class="form-check-label" for="gridRadios2">
                  Female
                </label>
            </div>
          </div>
        </fieldset>
        <div class="form-group row">
          <div class="col-sm-10">
            <button type="submit" class="btn btn-primary" @click.prevent="saveUser">Submit</button>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',

  data(){
    return{
      user:{
        mail:'',
        password:'',
        gender:''
      }
    }
  },

  methods:{
    saveUser(){
      console.log(this.user);
    }
  }
}
</script>


