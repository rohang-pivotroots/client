<template>
    <div class="row no-gutters">
        <section class="userSection my-3">
            <div>
                <p class="name">Name : <span class="font-weight-bold">{{user.name}}</span></p>
                <p class="username">Username : <span class="font-weight-bold">{{user.username}}</span></p>
                <p class="emailid">Email : <span class="font-weight-bold">{{user.email}}</span></p>
                <p class="phone">Phone : <span class="font-weight-bold">{{user.phone}}</span></p>
                <p>Website : <NuxtLink :to="user.website" class="website"><span class="font-weight-bold">{{user.website}}</span></NuxtLink></p>
            </div>
        </section>
    </div>
</template>

<script>
 export default{
     props: {
         user: {
             type: Object,
             default: () => {}
         }
     }
 }
</script>

<style scoped>
    .userSection{
        font-size: 16px;
        /* border: 1px solid #333; */
        /* border-radius: 10px; */
    }
    .userSection p{
        margin: 0;
    }
</style>