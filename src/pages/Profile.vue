<template>
  <div class="row">
    <div class="col-md-12">
      <card>
        <h4 slot="header">ผู้ใช้งานทั้งหมด</h4>
        <table class="table">
          <thead>
            <tr>
              <th scope="col"></th>
              <th scope="col">Name</th>
              <th scope="col">Email</th>
              <th scope="col">Status</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">1</th>
              <td>วิทย์</td>
              <td>test@gmail.com</td>
              <td> <p class="text-success">online</p> </td>
            </tr>
            <tr>
              <th scope="row">2</th>
              <td>ปอนด์</td>
              <td>test@gmail.com</td>
              <td> <p class="text-danger">offline</p> </td>
            </tr>
            <tr>
              <th scope="row">3</th>
              <td>ออม</td>
              <td>test@gmail.com</td>
              <td> <p class="text-success">online</p> </td>
            </tr>
            <tr>
              <th scope="row">2</th>
              <td>ปอ</td>
              <td>test@gmail.com</td>
              <td> <p class="text-danger">offline</p> </td>
            </tr>
          </tbody>
        </table>
      </card>
    </div> 
  </div>
</template>
<script>
  import EditProfileForm from './Profile/EditProfileForm';
  import UserCard from './Profile/UserCard'
  export default {
    components: {
      EditProfileForm,
      UserCard
    },
    // Data (hardcoded)
    data() {
      return {
        model: {
          company: 'Creative Code Inc.',
          email: 'mike@email.com',
          username: 'michael23',
          firstName: 'Mike',
          lastName: 'Andrew',
          address: 'Bld Mihail Kogalniceanu, nr. 8 Bl 1, Sc 1, Ap 09',
          city: 'Melbourne',
          country: 'Australia',
          about: 'Lamborghini Mercy, Your chick she so thirsty, I\'m in that two seat Lambo.'
        },
        user: {
          fullName: 'Mike Andrew',
          title: 'Ceo/Co-Founder',
          description: `Do not be scared of the truth because we need to restart the human foundation in truth And I love you like Kanye loves Kanye I love Rick Owens’ bed design but the back is...`,
        }
      }
    }
  }
</script>
<style>
</style>
