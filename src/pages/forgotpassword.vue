<template>
<card>
<div class="log">
    <div class="vue-tempalte">
        <form>
            <h3>Forgot Password</h3>

            <div class="form-group">
                <label>Email address</label>
                <input type="email" class="form-control form-control-lg" />
            </div>

            <button type="submit" class="btn btn-dark btn-lg">Reset password</button>

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