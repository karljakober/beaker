<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Date</th>
          <th>Event</th>
          <th>Amout</th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="user in users"
          :key="user.id">
          <td>{{ user.name }}</td>
          <td>{{ user.date }}}</td>
          <td>{{ user.event }}</td>
          <td>{{ user.amount }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class Tables extends Vue {
  users = [
    {
      name: "Morgan",
      date: "10/22/2018",
      event: "Donation",
      amount: "$60.00"
    },
    {
      name: "Josh",
      date: "10/21/2018",
      event: "Bits",
      amount: "200"
    },
    {
      name: "Karl",
      date: "10/20/2018",
      event: "Tiltify",
      amount: "$100.00"
    },
    {
      name: "Salman",
      date: "10/19/2018",
      event: "Donation",
      amount: "$30.00"
    },
    {
      name: "Charmili",
      date: "10/18/2018",
      event: "Bits",
      amount: "100"
    },
    {
      name: "Runxi",
      date: "10/18/2018",
      event: "Donation",
      amount: "$20.50"
    }
  ];
}
</script>
