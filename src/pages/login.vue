<template>
    <card>
    <div class="log">
    <div class="vue-tempalte">
        <form>
            <h3>Sign In</h3>

            <div class="form-group">
                <label>Email address</label>
                <input type="email" class="form-control form-control-lg" />
            </div>

            <div class="form-group">
                <label>Password</label>
                <input type="password" class="form-control form-control-lg" />
            </div>
            <br>
            <button type="submit" class="btn btn-dark btn-lg">Sign In</button>

            <p class="forgot-password text-right mt-2 mb-4">
                <br>
                <router-link to="/forgot-password">Forgot password</router-link>
            </p>
        </form>
    </div>
    </div>
    </card>
</template>

<script>
import Card from '../components/Cards/Card.vue'
    export default {
  components: { Card },
        data() {
            return {}
        }
    }
</script>
<style scoped>
.log{
    text-align: center;
    margin-left: 25%;
    margin-right: 25%;
}
</style>