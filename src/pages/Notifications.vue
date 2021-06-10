<template>
  <div class="row">
    <div class="col-md-6">
      <card>
        <h4 slot="header">เกี่ยวกับการเเจ้งเตือน</h4>
        <base-alert type="info">
          <span>This is a plain notification</span>
        </base-alert>
      </card>
    </div>
    <div class="col-md-6">
      <card>
        <h4 slot="header">แจ้งเตือนน้ำหนักขยะ</h4>
        <base-alert type="warning" dismissible>
          <span><b> ขวดเเก้ว - </b> ขณะนี้ขวดแก้วใกล้เต็มแล้วเตรียมเคลียร์ขยะในอีกไม่ช้า</span>
        </base-alert>
        <base-alert type="danger" dismissible>
          <span><b> ขวดพลาสติก - </b> ขณะนี้ขวดพลาสติกเต็มแล้วโปรดรีบเคลียร์ขยะด่วน</span>
        </base-alert>
      </card>
    </div>
    
  </div>
</template>
<script>
  import NotificationTemplate from './Notifications/NotificationTemplate';
  import { BaseAlert } from '@/components';

  export default {
    components: {
      BaseAlert
    },
    data() {
      return {
        type: ["", "info", "success", "warning", "danger"],
        notifications: {
          topCenter: false
        }
      };
    },
    methods: {
      notifyVue(verticalAlign, horizontalAlign) {
        const color = Math.floor(Math.random() * 4 + 1);
        this.$notify({
          component: NotificationTemplate,
          icon: "tim-icons icon-bell-55",
          horizontalAlign: horizontalAlign,
          verticalAlign: verticalAlign,
          type: this.type[color],
          timeout: 0
        });
      }
    }
  };
</script>
<style>
</style>
