<template>
  <div class="max-w-6xl mx-auto px-4">
    <h1 class="text-4xl text-center font-bold uppercase my-4">oswin.io</h1>
    <div class="flex flex-row flex-wrap">
      <ProfileCard
        class="w-full md:w-1/2"
        v-for="member in members"
        :key="member.id"
        :profile="member.profile"
      />
    </div>
  </div>
</template>

<script>
import ProfileCard from "@/components/ProfileCard";

export default {
  components: {
    ProfileCard
  },
  data() {
    return {
      members: {
        NicolasRoger: {
          profile: {
            name: "Nicolas Roger",
            job: "Creative Technologist @ Blackfoot.io",
            photo: "assets/jpg/nicolasroger.jpg",
            skills: {
              1: "Développement frond-end",
              2: "Modélisation 3D",
              3: "Photographie"
            },
            links: {
              instagram: {
                text: "instagram",
                url: "https://instagram.com/0sw.in"
              },
              linkedin: {
                text: "linkedin",
                url: "https://linkedin.com/nicolas9roger"
              },
              github: {
                text: "github",
                url: "https://github.com/0swin"
              },
              mail: {
                text: "mail",
                url: "mailto:nicolas@oswin.io"
              }
            }
          }
        },
        MelissaLuntadila: {
          profile: {
            name: "Mélissa Luntadila",
            job: "Graphic Designer",
            photo: "assets/jpg/melissaluntadila.jpg",
            skills: {
              1: "Identité graphique",
              2: "Illustration digitale",
              3: "Animation frame by frame"
            },
            links: {
              instagram: {
                text: "instagram",
                url: "https://instagram.com/melilunt"
              },
              linkedin: {
                text: "linkedin",
                url: "https://linkedin.com/in/melilun"
              },
              web: {
                text: "web",
                url: "https://melilun.ml"
              }
            }
          }
        }
      }
    };
  }
};
</script>

<style>
body {
  @apply bg-gray-300;
}
</style>