<template>
  <v-container
    id="regular-tables-view"
    fluid
    tag="section"
  >
    <view-intro
      heading="Monitoring"
      link="components/simple-tables"
    />

    <material-card
      icon="mdi-clipboard-text"
      icon-small
      title="Service"
      color="brown"
    >
      <v-simple-table>
        <thead>
          <tr>
            <th class="primary--text">
              name
            </th>
            <th class="primary--text">
              address
            </th>
            <th class="primary--text">
              status
            </th>
          </tr>
        </thead>

        <tbody>
          <tr
            v-for="deploy in deploys"
            :key="deploy.serviceId"
            @click="clickItem(deploy.name)"
          >
            <td>{{ deploy.name }}</td>
            <td>{{ deploy.address }}</td>
            <td>{{ deploy.status }}</td>
          </tr>
        </tbody>
      </v-simple-table>
    </material-card>

    <div class="py-3" />
  </v-container>
</template>

<script>
  import axios from 'axios'
  export default {
    name: 'RegularTablesView',
    data: function () {
      return {
        deploys: [],
      }
    },
    mounted: function () {
      axios.get('http://localhost:8080/api/v1/deploys', {
        params: {
          cluster_id: 'gn84rh5j1ibezbe7u5a48xeg1o',
          namespace: 180,
        },
      }).then(res => {
        for (var value of res.data) {
          this.deploys.push(value)
        }
      }).catch(err => { console.log(err) })
    },
    methods: {
      clickItem: function (displayName) {
        this.$router.push(`/dashboard/${displayName}`)
      },
    },
  }
</script>
