<template>
  <h1>Information</h1>
  <h3>Name: {{ Infomation.Name }}</h3>
  <h3>LastName: {{ Infomation.LastName }}</h3>
  <h3>Age: {{ Infomation.Age }}</h3>
  <h3>Contact:</h3>
  <router-link
    :to="{
      name: 'contact',
      params: {email: Infomation.Contact.Email ,phoneNumber: Infomation.Contact.PhoneNumber},
    }"
  >
    <p>Contact Info</p>
  </router-link>
</template>

<script>
export default {
  props: {
    Contact: Object,
  },
  data: () => ({
    Infomation: {
      Name: 'Thanasit',
      LastName: 'Eksoragul',
      Age: 20,
      Skill: 'java spring boot',
      Contact: {
        Email: 'thanasit.eksoragul@mail.kmutt.ac.th',
        PhoneNumber: '0869769873',
      },
    },
  }),
};
</script>
