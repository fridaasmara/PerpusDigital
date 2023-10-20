<template>
  <div>
    <table border="1" width="100%">
      <thead>
        <tr>
          <th>No</th>
          <th>tanggal</th>
          <th>nama</th>
          <th>kategori</th>
          <th>keperluan</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(pengunjung, index) in visitors" :key="pengunjung.id">
          <td>{{ index + 1 }}</td>
          <td>{{ pengunjung.tanggal }}</td>
          <td>{{ pengunjung.nama }}</td>
          <td>{{ pengunjung.kategori }}</td>
          <td>{{ pengunjung.keperluan }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
const client = useSupabaseClient();
const visitors = ref([]);

async function getData() {
  const { data, error } = await client.from("table-data-pengunjung").select();
  if (data) visitors.value = data;
}

onMounted(() => getData());
</script>

<style lang="scss" scoped></style>
