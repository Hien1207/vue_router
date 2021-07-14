<template>
  <div>
    <div class="container" style="margin-bottom:50px">
    <div class="container-left">
      <div>
        <img :src="activeBlog.avatar" :alt="activeBlog.title" />
      </div>
    </div>
     <div class="container-left">
      <div>
        <h1 class="titled">{{ activeBlog.name }}</h1>
        <p class="textd">{{ activeBlog.phoneNumber }}</p>
        <p class="textd">{{ activeBlog.gmail }}</p>
        <p class="contentt">Artificial Intelligence (AI) can be confusing. AI is a broad term that covers a wide range of applications, 
          and while we see AI technologies performing a swath of incredible feats such as Google Translate, AlphaGo, and solving a
          rubik's cube, it can be hard to tell which business problems AI is apt to solve. Matching a given problem to an AI solution
           often comes down to framing: sometimes what appears as an intractable problem can, with minor tweaks, become the kind of proble
           AI excels at solving. </p>     
       <p class="contentt">At Impira, we’ve been fortunate to work through these challenges with customers across a variety of industries, departments,
          and use cases. As part of that process, we’ve developed an internal framework to help customers evaluate how AI can be used 
          to automate their manual workflows around unstructured data (i.e., images, videos, and scanned documents). Here, we’ll share 
          how we think about that framework and some examples of problems for which AI can make a meaningful difference.</p>
       </div>
     </div>
    </div>
</div>
</template>

<script>
export default {
  name: "blogdetail",
  computed: {
    activeBlog() {
      return this.users[this.$route.params.id-1];
    },
  },
  data: () => {
     return {
      users: [
        {
         "createdAt": "2021-07-07T20:58:41.253Z",
         "name": "Roosevelt Johnson III",
         "avatar": "https://assets-global.website-files.com/5e3898dff5077817ea80d71c/602368e608f00aa08d892242_Impira%20AutoML-half-min.png",
         "gmail": "Laurianne90@yahoo.com",
         "phoneNumber": "(856) 254-9123 x7594",
         "id": "1"
        },
        {
         "createdAt": "2021-07-07T18:29:22.811Z",
         "name": "Geneva Smith",
         "avatar": "https://assets-global.website-files.com/5e3898dff5077817ea80d71c/5ffe2c58bd6dfb7fb7390e37_IDC%20podcasts%40half-min.png",
         "gmail": "Yolanda_Mayer@yahoo.com",
         "phoneNumber": "(265) 403-3362 x414",
         "id": "2"
        },
        {
         "createdAt": "2021-07-08T11:52:20.212Z",
         "name": "Brian Mills",
         "avatar": "https://assets-global.website-files.com/5e3898dff5077817ea80d71c/5e3a71a0d565b243a03a300f_chair%20with%20cat500x500-min.png",
         "gmail": "Gaetano22@gmail.com",
         "phoneNumber": "763.294.4416 x87790",
         "id": "3"
        },
        {
         "createdAt": "2021-07-08T08:33:06.971Z",
         "name": "Lindsey Hills",
         "avatar": "https://assets-global.website-files.com/5e3898dff5077817ea80d71c/5e67ca67a22e4e9f8038cb14_evaluating-AI500x500.png",
         "gmail": "Maegan.Hodkiewicz35@yahoo.com",
         "phoneNumber": "301-486-6216",
         "id": "4"
        },
        {
         "createdAt": "2021-07-07T16:52:43.691Z",
         "name": "Tom Veum",
         "avatar": "https://assets-global.website-files.com/5e3898dff5077817ea80d71c/5e7a2ac929bff5a8de51a5df_what%20not%20how500x500.png",
         "gmail": "Erin11@hotmail.com",
         "phoneNumber": "538.597.0983 x20328",
         "id": "5"
        },
        {
         "createdAt": "2021-07-08T06:29:13.969Z",
         "name": "Felipe Welch",
         "avatar": "https://cdn.fakercloud.com/avatars/mohanrohith_128.jpg",
         "gmail": "Merritt19@gmail.com",
         "phoneNumber": "604-688-1217",
         "id": "6"
        },
        {
         "createdAt": "2021-07-07T14:31:36.301Z",
         "name": "Misty Greenholt",
         "avatar": "https://cdn.fakercloud.com/avatars/edgarchris99_128.jpg",
         "gmail": "Jolie_Wisozk64@yahoo.com",
         "phoneNumber": "308-383-7198",
         "id": "7"
        },
        {
         "createdAt": "2021-07-07T14:57:58.146Z",
         "name": "Kyle Bergstrom",
         "avatar": "https://cdn.fakercloud.com/avatars/smenov_128.jpg",
         "gmail": "Daija27@gmail.com",
         "phoneNumber": "(459) 938-7947 x1371",
         "id": "8"
        },
        {
         "createdAt": "2021-07-08T04:11:02.598Z",
         "name": "Mrs. Kelley Adams",
         "avatar": "https://cdn.fakercloud.com/avatars/jlsolerdeltoro_128.jpg",
         "gmail": "Darrell.Padberg50@yahoo.com",
         "phoneNumber": "693.538.0400",
         "id": "9"
        },
        {
         "createdAt": "2021-07-07T14:22:24.960Z",
         "name": "Antonia Langworth",
         "avatar": "https://cdn.fakercloud.com/avatars/juanmamartinez_128.jpg",
         "gmail": "Retta_Ward@yahoo.com",
         "phoneNumber": "681-264-3024",
         "id": "10"
        },
        {
         "createdAt": "2021-07-08T11:41:03.238Z",
         "name": "Diane Koelpin",
         "avatar": "https://cdn.fakercloud.com/avatars/vaughanmoffitt_128.jpg",
         "gmail": "Darwin.Smitham@hotmail.com",
         "phoneNumber": "(366) 336-8149 x3498",
         "id": "11"
        },
        {
         "createdAt": "2021-07-07T20:17:41.012Z",
         "name": "Katherine Barrows III",
         "avatar": "https://cdn.fakercloud.com/avatars/leandrovaranda_128.jpg",
         "gmail": "Aliya.Barrows@hotmail.com",
         "phoneNumber": "(980) 842-0659",
         "id": "12"
        },
        {
         "createdAt": "2021-07-08T00:37:29.364Z",
         "name": "Lila Harris",
         "avatar": "https://cdn.fakercloud.com/avatars/stushona_128.jpg",
         "gmail": "Isabel.Gusikowski@hotmail.com",
         "phoneNumber": "891.596.9849",
         "id": "13"
        },
        {
         "createdAt": "2021-07-08T10:18:35.012Z",
         "name": "Gertrude Gusikowski",
         "avatar": "https://cdn.fakercloud.com/avatars/exentrich_128.jpg",
         "gmail": "Elvera78@hotmail.com",
         "phoneNumber": "941.755.8625 x56596",
         "id": "14"
        },
        {
         "createdAt": "2021-07-07T20:24:43.734Z",
         "name": "Miss Jack Douglas",
         "avatar": "https://cdn.fakercloud.com/avatars/koridhandy_128.jpg",
         "gmail": "Christiana.Cruickshank14@gmail.com",
         "phoneNumber": "561.721.9399",
         "id": "15"
        },
        {
         "createdAt": "2021-07-07T13:44:43.833Z",
         "name": "Mrs. Sara Schuster",
         "avatar": "https://cdn.fakercloud.com/avatars/edhenderson_128.jpg",
         "gmail": "Gardner4@gmail.com",
         "phoneNumber": "652-571-2854",
         "id": "16"
        },
        {
         "createdAt": "2021-07-08T03:16:48.296Z",
         "name": "Edmond Kertzmann",
         "avatar": "https://cdn.fakercloud.com/avatars/robergd_128.jpg",
         "gmail": "Libbie.Weissnat@yahoo.com",
         "phoneNumber": "451-488-0178 x64538",
         "id": "17"
        },
        {
         "createdAt": "2021-07-07T16:09:21.859Z",
         "name": "Tammy Mayert",
         "avatar": "https://cdn.fakercloud.com/avatars/iamglimy_128.jpg",
         "gmail": "Dante_Klocko13@gmail.com",
         "phoneNumber": "959-604-4418",
         "id": "18"
        },
        {
         "createdAt": "2021-07-07T23:28:13.120Z",
         "name": "Mrs. Thelma Howe",
         "avatar": "https://cdn.fakercloud.com/avatars/mvdheuvel_128.jpg",
         "gmail": "Pauline.Gerhold@gmail.com",
         "phoneNumber": "(769) 581-5939",
         "id": "19"
        },
        {
         "createdAt": "2021-07-08T04:57:02.648Z",
         "name": "Lillie Dickens",
         "avatar": "https://cdn.fakercloud.com/avatars/juamperro_128.jpg",
         "gmail": "Derick_Yost94@yahoo.com",
         "phoneNumber": "(872) 636-1162 x611",
         "id": "20"
        },
        {
         "createdAt": "2021-07-10T06:49:25.775Z",
         "name": "Terrance Olson",
         "avatar": "https://cdn.fakercloud.com/avatars/vikasvinfotech_128.jpg",
         "gmail": "Kyler.Schmeler@hotmail.com",
         "phoneNumber": "(755) 451-6175 x590",
         "id": "21"
        },
        {
         "createdAt": "2021-07-10T07:48:42.262Z",
         "name": "Ms. Eloise Bogisich",
         "avatar": "https://cdn.fakercloud.com/avatars/sur4dye_128.jpg",
         "gmail": "Lucas57@yahoo.com",
         "phoneNumber": "342-720-8841 x4139",
         "id": "22"
        },
        {
         "createdAt": "2021-07-10T01:27:26.139Z",
         "name": "Josefina Sanford",
         "avatar": "https://cdn.fakercloud.com/avatars/myastro_128.jpg",
         "gmail": "Abdul6@yahoo.com",
         "phoneNumber": "(679) 609-2688",
         "id": "23"
        },
        {
         "createdAt": "2021-07-09T17:20:11.205Z",
         "name": "Louis Bahringer",
         "avatar": "https://cdn.fakercloud.com/avatars/ipavelek_128.jpg",
         "gmail": "Bart.Kshlerin@hotmail.com",
         "phoneNumber": "(536) 958-3258",
         "id": "24"
        },
        {
         "createdAt": "2021-07-09T21:27:32.692Z",
         "name": "Mr. May Blick",
         "avatar": "https://cdn.fakercloud.com/avatars/sgaurav_baghel_128.jpg",
         "gmail": "Fletcher_Heaney@yahoo.com",
         "phoneNumber": "1-681-546-0508 x26131",
         "id": "25"
        },
        {
         "createdAt": "2021-07-10T02:18:30.807Z",
         "name": "Jesus Weissnat DDS",
         "avatar": "https://cdn.fakercloud.com/avatars/muridrahhal_128.jpg",
         "gmail": "Richard18@gmail.com",
         "phoneNumber": "509-329-9830",
         "id": "26"
        },
        {
         "createdAt": "2021-07-09T19:58:46.958Z",
         "name": "Caleb Rippin",
         "avatar": "https://cdn.fakercloud.com/avatars/gaborenton_128.jpg",
         "gmail": "Joel.Kuhlman@hotmail.com",
         "phoneNumber": "538.722.0871 x71321",
         "id": "27"
        },
        {
         "createdAt": "2021-07-10T09:51:34.781Z",
         "name": "Ms. William Torp",
         "avatar": "https://cdn.fakercloud.com/avatars/thedjpetersen_128.jpg",
         "gmail": "Aiden.Tillman@hotmail.com",
         "phoneNumber": "1-516-804-4206 x01869",
         "id": "28"
        },
        {
         "createdAt": "2021-07-09T22:59:48.976Z",
         "name": "Lynne Cummings DVM",
         "avatar": "https://cdn.fakercloud.com/avatars/d_kobelyatsky_128.jpg",
         "gmail": "Nicklaus_Waelchi@hotmail.com",
         "phoneNumber": "(315) 429-3849",
         "id": "29"
        },
        {
         "createdAt": "2021-07-09T17:03:02.239Z",
         "name": "Melinda Kovacek",
         "avatar": "https://cdn.fakercloud.com/avatars/rodnylobos_128.jpg",
         "gmail": "Gordon.Padberg95@yahoo.com",
         "phoneNumber": "481-733-8340",
         "id": "30"
        },
        {
         "createdAt": "2021-07-10T06:02:25.388Z",
         "name": "Jerald Schowalter",
         "avatar": "https://cdn.fakercloud.com/avatars/traneblow_128.jpg",
         "gmail": "Mazie_Thompson14@gmail.com",
         "phoneNumber": "866.614.9243",
         "id": "31"
        },
        {
         "createdAt": "2021-07-10T11:48:47.853Z",
         "name": "Fernando McClure",
         "avatar": "https://cdn.fakercloud.com/avatars/uxalex_128.jpg",
         "gmail": "Melvina_Berge@yahoo.com",
         "phoneNumber": "(647) 302-1408",
         "id": "32"
        },
        {
         "createdAt": "2021-07-10T01:59:37.993Z",
         "name": "Zachary Bosco",
         "avatar": "https://cdn.fakercloud.com/avatars/mylesb_128.jpg",
         "gmail": "Alysha_OConnell79@hotmail.com",
         "phoneNumber": "(609) 393-9090 x51988",
         "id": "33"
        },
        {
         "createdAt": "2021-07-10T07:51:32.900Z",
         "name": "Carl Gaylord II",
         "avatar": "https://cdn.fakercloud.com/avatars/psaikali_128.jpg",
         "gmail": "Celine.Leffler@gmail.com",
         "phoneNumber": "1-784-645-3841",
         "id": "34"
        },
        {
         "createdAt": "2021-07-10T11:11:07.198Z",
         "name": "Rhonda Nicolas",
         "avatar": "https://cdn.fakercloud.com/avatars/vlajki_128.jpg",
         "gmail": "Patience.Marquardt77@gmail.com",
         "phoneNumber": "923-535-7231",
         "id": "35"
        },
        {
         "createdAt": "2021-07-10T02:04:03.793Z",
         "name": "Rogelio Green",
         "avatar": "https://cdn.fakercloud.com/avatars/emsgulam_128.jpg",
         "gmail": "Audra38@yahoo.com",
         "phoneNumber": "476-594-8967 x100",
         "id": "36"
        },
        {
         "createdAt": "2021-07-10T02:19:47.999Z",
         "name": "Ms. Joseph Pfeffer",
         "avatar": "https://cdn.fakercloud.com/avatars/richardgarretts_128.jpg",
         "gmail": "Riley.Terry8@gmail.com",
         "phoneNumber": "338.265.4373",
         "id": "37"
        },
        {
         "createdAt": "2021-07-09T16:59:45.374Z",
         "name": "Judy Pouros IV",
         "avatar": "https://cdn.fakercloud.com/avatars/tomas_janousek_128.jpg",
         "gmail": "Herman19@yahoo.com",
         "phoneNumber": "(212) 507-6005 x486",
         "id": "38"
        },
        {
         "createdAt": "2021-07-10T11:22:31.151Z",
         "name": "Arturo Leuschke",
         "avatar": "https://cdn.fakercloud.com/avatars/vm_f_128.jpg",
         "gmail": "Alba.Frami@hotmail.com",
         "phoneNumber": "926.647.6815 x3970",
         "id": "39"
        },
        {
         "createdAt": "2021-07-10T12:49:28.460Z",
         "name": "Maurice Auer",
         "avatar": "https://cdn.fakercloud.com/avatars/andrewofficer_128.jpg",
         "gmail": "Noemy.Swift93@hotmail.com",
         "phoneNumber": "(430) 581-3137 x8025",
         "id": "40"
        }
       ]
    };
  }
};
</script>

<style>
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
  width: 40%;
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
.titled {
  text-transform: capitalize;
  margin-bottom: 10px;
  font-size: 40px;
}
.textd{
  font-size: 20px;
  color: gray;
  margin-bottom: 5px;
}
.contentt{
  font-size: 18px;
}
</style>