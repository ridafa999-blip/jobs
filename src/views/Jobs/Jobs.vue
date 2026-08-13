<template>
  <h1>Jobs</h1>
  <!-- تعديل: تغيير class="job" إلى class="job" لتنسيق الـ CSS أو توحيد المسمى -->
  <div v-for="job in jobs" :key="job.id" class="job">
    <!-- تعديل: تغيير اسم المسار من 'jobsDetails' إلى 'jobDetails' (بدون حرف s) ليطابق index.js -->
    <router-link :to="{ name: 'jobDetails', params: { id: job.id } }">
      <h2>{{ job.title }}</h2>
    </router-link>
  </div>
</template>

<script>
export default {
  data(){
    return {
      jobs:[
        { title: 'Ninja UX Designer', id: 1, details: 'lorem' },
        { title: 'Ninja Web Developer', id: 2, details: 'lorem' },
        { title: 'Ninja Vue Developer', id: 3, details: 'lorem' },
      ]
    }
  }
}
</script>

<style>
/* تعديل: تغيير .jobs إلى .job لتطابق اسم Class في الـ HTML */
.job {
  background: #faf4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
/* تعديل: إصلاح التنسيق */
.job h2:hover {
  background: #ddd;
}
.job a {
  text-decoration: none;
}
</style>