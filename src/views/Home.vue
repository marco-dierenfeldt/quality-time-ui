<template>
  <div>
    <HelloWorld msg="Welcome to Quality Time!" />
    <hr>
    <TimeEntryList></TimeEntryList>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import TimeEntryList from '@/components/TimeEntryList.vue';
export default {
  name: "home",
  components: {
      HelloWorld,
      TimeEntryList
  }
};
</script>
