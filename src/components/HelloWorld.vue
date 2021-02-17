<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <section>
      <h3>Static contact</h3>
      <nylas-contact-list
        id="428e0de5-9a87-4257-b20c-714d77dfd8c7"
        :contacts="contacts" />
    </section>
    <section>
      <h3>No contacts</h3>
      <nylas-contact-list
        id="428e0de5-9a87-4257-b20c-714d77dfd8c7"
        :contacts="noContacts" />
    </section>
  </div>
</template>

<script>
import '@nylas/components-contact-list';
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }, 
  data () {
    return {
      noContacts: [],
      contacts: [
      {
        account_id: "none",
        birthday: null,
        company_name: null,
        emails: [{ email: "nylascypresstest@gmail.com", type: "work" }],
        given_name: "Nylas Contact #1",
        id: "string",
        source: null,
        im_addresses: [],
        job_title: null,
        manager_name: null,
        middle_name: null,
        nickname: null,
        notes: null,
        object: "object",
        office_location: null,
        phone_numbers: [],
        physical_addresses: [],
        picture_url: null,
        suffix: null,
        surname: null,
        web_pages: [],
        groups: [],
      }
    ]
    }
  }
}
</script>

<style scoped>
section {
  padding: 40px;
  background-color: #42b983;
  border-bottom: 4px solid white;
}
h3 {
  margin: 20px 0 20px;
}
a {
  color: #42b983;
}
</style>
