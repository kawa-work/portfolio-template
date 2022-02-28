<template>
  <v-card id="basic" class="my-12" flat>
    <v-card-title> Basic Info </v-card-title>
    <v-card-text>
      <v-simple-table>
        <template #default>
          <tbody>
            <tr v-for="item in info" :key="item.name">
              <td>{{ item.name }}</td>
              <td>{{ item.val }}</td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      info: [
        {
          name: '名前',
          val: 'サンプル名前',
        },
        {
          name: '年齢',
          val: 'サンプル年齢',
        },
        {
          name: '希望職種',
          val: 'サンプル職種',
        },
      ],
    }
  },
}
</script>