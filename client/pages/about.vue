<script setup>
definePageMeta({
  layout: "landing",
});

const TeamImg1 = "https://scontent.fmnl13-2.fna.fbcdn.net/v/t39.30808-6/352523250_3654625484824132_2131867550000553666_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeFLA7dphonRk7q2Cf4AFyufs7zPdVudTxuzvM91W51PGympa1IklzvWycWoLVYs-pZM79WdvL_ZJzIUV5sppe2G&_nc_ohc=xG2_Y6IblsAQ7kNvgEoZ_z6&_nc_ht=scontent.fmnl13-2.fna&oh=00_AfDSHe-qBuJue7pj3eHPWddd33VRFINS-JbiEVrbpEH5kQ&oe=6642B64C";
const TeamImg2 = "https://scontent-mnl1-2.xx.fbcdn.net/v/t39.30808-6/367406410_2642432715920826_2233731413766194305_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeGrEgobTPM2UYePXiR0CnbZlG67vreePAKUbru-t548Aj80Jjq-jT6dUnG1lSzUvb3Ne_tA1MoVSFOe4UFmpLpX&_nc_ohc=cLBIvLsG3lIQ7kNvgEDiEns&_nc_ht=scontent-mnl1-2.xx&oh=00_AfAtTvvMyg5SDqLPuX5vhQxjzVTN-i5GEklniqCncdrZMg&oe=664287AE";
const TeamImg3 = "https://scontent.fmnl13-2.fna.fbcdn.net/v/t39.30808-6/433966529_1085149662809482_1169174252083751668_n.jpg?stp=cp6_dst-jpg&_nc_cat=101&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeHnlHwiamjKEJpsfej8HliwYE8kKScW2mpgTyQpJxbaaqd2fDyOqdX0Q1Gt8gr7LAJaoD331AhqDFhZf8mL9wnr&_nc_ohc=Sm5RQl6xEdgQ7kNvgHD4--v&_nc_ht=scontent.fmnl13-2.fna&oh=00_AfBjgb3sG7x9nff6lt56HZf1mKMYEvnTZLbsRQ26iYSwiQ&oe=6642A613";

const team = [
  {
    name: "Heinz Kyle",
    title: "Senior Director",
    avatar: {
      src: TeamImg1,
      width: 480,
      height: 560,
    },
  },
  {
    name: "Froy Angelo",
    title: "Principal Strategist",
    avatar: {
      src: TeamImg2,
      width: 580,
      height: 580,
    },
  },
  {
    name: "Robert Jims",
    title: "Marketing Engineer",
    avatar: {
      src: TeamImg3,
      width: 580,
      height: 580,
    },
  },
];
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>About</template>
      <template v-slot:desc>We are a small passionate team.</template>
    </LandingSectionhead>

    <div class="flex flex-col gap-3 mx-auto max-w-4xl mt-16">
      <h2 class="font-bold text-3xl text-gray-800">
        Empowering the world with Nuxt.
      </h2>
      <p class="text-lg leading-relaxed text-slate-500">
        We're a multi-cultural team from around the world! We come from diverse
        backgrounds, bringing different personalities, experiences and skills to
        the job. This is what makes our team so special.
      </p>
    </div>
    <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-4xl mt-12">
      <div v-for="item of team" class="group">
        <div class="w-full aspect-square">
          <img
            :src="item.avatar.src"
            :width="item.avatar.width"
            :height="item.avatar.height"
            format="avif"
            alt="Team"
            class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
          />
        </div>

        <div class="mt-4 text-center">
          <h2 class="text-lg text-gray-800">{{ item.name }}</h2>
          <h3 class="text-sm text-slate-500">{{ item.title }}</h3>
        </div>
      </div>
      <!-- {
        team.map((item) => (
          <div class="group">
            <div class="w-full aspect-square">
              <Image
                {...item.avatar}
                format="avif"
                alt="Team"
                class="w-full h-full object-cover rounded transition  group-hover:-translate-y-1 group-hover:shadow-xl"
              />
            </div>

            <div class="mt-4 text-center">
              <h2 class="text-lg text-gray-800"> {item.name}</h2>
              <h3 class="text-sm text-slate-500"> {item.title}</h3>
            </div>
          </div>
        ))
      } -->
    </div>
  </LandingContainer>
</template>
