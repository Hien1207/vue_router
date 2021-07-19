<template>
  <div>
    <div class="container">
    <div class="container-left"  style="margin-top:60px">
        <strong> Company / 2  min read</strong>
        <br>
        <br>
        <a href="/blog/announcing-our-zapier-integration" class="inline-block">
           <h1 class="hero__header">Announcing our Zapier integration</h1>
        </a>
        <strong style="font-weight:500">By the team at Impira / June 22, 2021 </strong>
        <br>
        <br>
        <p class="p-text">At Impira, we’re driven by the goal of removing repetitive manual tasks that hamper productivity and keep you from doing what you do best. Sometimes, we’re able to link arms with other like-minded solutions to give our users more opportunities to save themselves from data entry dread.</p>
        <div class="email-form"> 
              <a class="form">Try for free</a>
            </div>
    </div>
     <div class="container-left">
       <img src="https://assets-global.website-files.com/5e3898dff5077817ea80d71c/60ca686e9c2e661b9c44c9d9_202106-zapier%20x%20impira-square.png" class="contained-image">
     </div>
    </div>
    <div class="pagi">
       <b-pagination
        v-model="page"
        :total-rows="count"
        :per-page="pageSize"
        prev-text="Prev"
        next-text="Next"
      ></b-pagination>
    </div>   
    <div class="container" style="margin: 5% 8%">
        <div
          class="post"
          :class="{ active: index == currentIndex }"
          v-for="(user,index) in displayedUsers"
          :key="index"
          @click="$router.push('/blog/' + user.id)"
        >
              <div class="image">
            <img :src="user.avatar" :alt="user.title" />
          </div>
          <div class="text">
            <h4 class="title">{{ user.name }}</h4>
            <p class="categoryId">{{ user.phoneNumber }}</p>
            <p class="content">{{ user.gmail }}</p>
         </div>
        </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: "blog",
  data: () => {
    return {
      users: [],
      baseUrl: 'http://localhost:3000/',
      currentUser: null,
      currentIndex: -1,
      page: 1,
      count: 40,
      pageSize: 5,
      perPage: 5,
      pages: [],
    };
  },
  async created(){
    try{const response = await axios.get(this.baseUrl+'users')
    this.users = response.data;
    }
    catch(err){
      console.log(err);
    }
 },
  methods: {
    paginate (users) {
      let page = this.page;
      let perPage = this.perPage;
      let from = (page * perPage) - perPage;
      let to = (page * perPage);
      return  users.slice(from, to);
    }
  },
  computed: {
    displayedUsers () {
      return this.paginate(this.users);
    }
  },
};
</script>

<style lang="scss">
.h2 {
  font-size: 15px;
  text-transform: capitalize;
  font-weight: 700;
  font-style: italic;
}
.post {
  display: block;
  margin: 10px 0;
  cursor: pointer;
  margin-right: 30px;
}
.image {
  width: 230px;
  img {
    width: 90%;
    height: 90%;
    object-fit: cover;
    transition:transform .5s; ;
    opacity: 0.8;
  }
  img:hover{
     transform: scale(0.8);
  }
}
.text {
  width: 200px;
  padding-left:10px;
  text-align: center;
}
.title {
  text-transform: capitalize;
  margin-bottom: 5px;
}
.categoryId {
  margin: 5px 0;
  color: gray;
}
.content {
  color: gray;
}
a{
    background-color: transparent;
    color: black;
    text-decoration: none;
}
.inline-block{
  max-width: 100%;
  display: inline-block;
  margin-bottom: 20px;
}
a:hover{
  text-decoration: underline;
}
.email-form{
    width: 200px;
    height: 50px;
    margin-top: 20px;
    margin-bottom: 8px;
}
.form{
   display: inline-block;
    min-height: 30px;
    padding: 10px 24px 8px;
    background-color: white;
     border:2px solid black;
    color: black;
    line-height: 2;
    font-weight: 500;
    letter-spacing: .25px;
    cursor: pointer;
    transition:all 0.5s ease-in-out ;
}
.form:hover{
  background: black;
  color: white;
  text-decoration: none;
}
.container{
    position: relative;
    z-index: 3;
    display: flex;
    width: 90%;
    max-width: none;
    margin-right: 5%;
    margin-left: 5%;
    background-color: transparent;
}
.container-left{
  width: 50%;
  display: block;
    overflow: visible;
    height: auto;
    max-width: 960px;
    min-height: 0;
    min-width: 0;
    margin-left: 0;
    padding-top: 24px;
    padding-left: 36px;
    padding-right: 36px;
}
.contained-image{
  width: 100%;
    max-width: 600px;
    margin-right: 0;
    margin-left: 0;
    padding: 32px 0 32px 32px;
    align-self: center;
}
.hero__header{
  margin-top: 0;
    margin-bottom: 24px;
    font-size: 80px;
    line-height: 1;
    text-align: left;
    font-weight: 1;
}
.pagi{
  width: 40%;
  height: 20%;
  margin: 50px 600px;
  font-family: "Courier New", Courier, monospace;
}
</style>
