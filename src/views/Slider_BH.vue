<template>
    <div class="content">
      <v-sheet v-for="(group, groupIndex) in imageGroups" :key="groupIndex" class="image-container">
        <v-row>
          <v-col v-for="(item, index) in group" :key="index" class="image-col">
            <div class="image-wrapper">
                <v-img :src="item.image" contain class="v-image" :class="{ 'small-image': item.smallImage, 'smaller-image': item.smallerImage }"></v-img>
                <div class="image-text" style="white-space: pre;">
                    <div class="text-content">
                        <span class="title">{{ item.title }}</span>
                        <span class="text">{{ item.text }}</span>
                    </div>
                </div>
            </div>
          </v-col>
        </v-row>
      </v-sheet>
      <v-spacer style="background-color: #000000; height: 15vh;"></v-spacer>
    </div>
  </template>
  
  
  <script>

  export default {
    data() {
      return {
        imageGroups: [
            [
            
            ],
            [
                { image: "/portfolio/BH/BH_10.png", smallerImage: true}
            ],
            [
                {text: "2021. 09 ~ 2021. 12 \n\n Adobe XD, WordPress를 활용한 온라인 전시회 페이지 구축 \n Adobe XD, WordPress를 활용한 갤러리 소개 페이지 구축 \n Adobe Photoshop을 활용한 전시회 로고, 포스터, 티켓 디자인 \n Adobe After Effects를 활용한 전시회 인트로 작업 \n 안드로이드 버전 어플리케이션 작업  \n" }
            ],
            [
                
            ],
            [
                { image: "/portfolio/BH/BH_M.jpg"},
                { image: "/portfolio/BH/BH_G.jpg"},
                { image: "/portfolio/BH/BH_GA.jpg"},
                { image: "/portfolio/BH/BH_C.jpg"},
            ],
            [
                { image: "/portfolio/BH/BH_7.png"},
                { image: "/portfolio/BH/BH_8.png"},
            ],
            [
                { image: "/portfolio/BH/BH_9.png"},
                { image: "/portfolio/BH/BH_5.png"},
                { image: "/portfolio/BH/BH_6.png"},
            ],
        ]
      }
    },
    mounted() {
    window.scrollTo(0, 0);
    }
  }
  </script>
  
  <style scoped>
  .content {
    background-color: #000000;
  }
  
  .v-image {
    width: 100%;
    height: 100%;
  }
  
  .image-container {
    padding: 3% 10% 3% 10%;
    background-color: transparent;
  }

  .image-wrapper {
    text-align: center; /* 이미지와 텍스트 가로로 중앙 정렬 */
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  
  .image-col {
    text-align: center; /* 이미지와 텍스트 가로로 중앙 정렬 */
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .small-image {
    width: 75%;
    height: 75%;
  }

  .smaller-image {
    width: 25%;
    height: 25%;
  }
  
  .image-text {
    text-align: center;
    color: #ffffff;
  }
  
  .text-content {
    margin: -20% 0 5% 0 ; 
  }

  .title {
  font-size: 30px;
  font-family: 'GothicA1-ExtraBold', sans-serif;
  /* 추가로 원하는 스타일을 적용하세요 */
}

.text {
  font-size: 13px;
  font-family: 'GothicA1-Bold', sans-serif;
  line-height: 200%;
  /* 추가로 원하는 스타일을 적용하세요 */
}
  </style>