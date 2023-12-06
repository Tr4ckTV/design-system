<script setup>
definePageMeta({
  layout: "docs",
});
</script>

<template>
  <Container>
    <TitresH1> Layouts </TitresH1>

    <TextesParagraphe>
      Utilisez les layouts pour définir la structure de vos pages.
    </TextesParagraphe>

    <TitresH2> App Layout </TitresH2>

    <div class="ring-2 ring-gray-200/75 my-8">
      <LayoutsBase>
        <template #navigation>
          <NavsDocsNavigation />
        </template>

        <template #content>
          <Container>
            <div class="area">
              <ul class="circles">
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
              </ul>
            </div>
          </Container>
        </template>

        <template #footer>
          <FootersBasic />
        </template>
      </LayoutsBase>
    </div>

    <TextesCode
      :code="`<LayoutsBase>
    <template #navigation>
        <NavsDocsNavigation />
    </template>

    <template #content>
        <Container>
            <div>Contenu de la page</div>
        </Container>
    </template>

    <template #footer>
        <FootersBasic />
    </template>
</LayoutsBase>`"
    />

    <TitresH2> Container </TitresH2>

    <TextesCode
      :code="`<Container>
    Contenu
</Container>
`"
    />
  </Container>
</template>

<style scoped>
/*Start Animations*/
@-webkit-keyframes animatetop {
  from {
    top: -300px;
    opacity: 0;
  }
  to {
    top: 0;
    opacity: 1;
  }
}
@keyframes animatetop {
  from {
    top: -300px;
    opacity: 0;
  }
  to {
    top: 0;
    opacity: 1;
  }
}
@-webkit-keyframes zoomIn {
  0% {
    opacity: 0;
    -webkit-transform: scale3d(0.3, 0.3, 0.3);
    transform: scale3d(0.3, 0.3, 0.3);
  }
  50% {
    opacity: 1;
  }
}
@keyframes zoomIn {
  0% {
    opacity: 0;
    -webkit-transform: scale3d(0.3, 0.3, 0.3);
    transform: scale3d(0.3, 0.3, 0.3);
  }
  50% {
    opacity: 1;
  }
}
/*End Animations*/
/*
-- Start BackGround Animation 
*/
.area {
  background: #4e54c8;
  background: -webkit-linear-gradient(to left, #8f94fb, #4e54c8);
  width: 86.79%;
  height: 88.73vh;
  position: absolute;
  top: 458px;
  left: 95px;
}

.circles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 96%;
  overflow: hidden;
}

.circles li {
  position: absolute;
  display: block;
  list-style: none;
  width: 20px;
  height: 20px;
  background: rgb(255, 0, 0);
  animation: animate 25s linear infinite;
  bottom: -150px;
}

.circles li:nth-child(1) {
  left: 25%;
  width: 80px;
  height: 80px;
  animation-delay: 0s;
}

.circles li:nth-child(2) {
  left: 10%;
  width: 20px;
  height: 20px;
  animation-delay: 2s;
  animation-duration: 12s;
}

.circles li:nth-child(3) {
  left: 70%;
  width: 20px;
  height: 20px;
  animation-delay: 4s;
}

.circles li:nth-child(4) {
  left: 40%;
  width: 60px;
  height: 60px;
  animation-delay: 0s;
  animation-duration: 18s;
}

.circles li:nth-child(5) {
  left: 65%;
  width: 20px;
  height: 20px;
  animation-delay: 0s;
}

.circles li:nth-child(6) {
  left: 75%;
  width: 110px;
  height: 110px;
  animation-delay: 3s;
}

.circles li:nth-child(7) {
  left: 35%;
  width: 150px;
  height: 150px;
  animation-delay: 7s;
}

.circles li:nth-child(8) {
  left: 50%;
  width: 25px;
  height: 25px;
  animation-delay: 15s;
  animation-duration: 45s;
}

.circles li:nth-child(9) {
  left: 20%;
  width: 15px;
  height: 15px;
  animation-delay: 2s;
  animation-duration: 35s;
}

.circles li:nth-child(10) {
  left: 85%;
  width: 150px;
  height: 150px;
  animation-delay: 0s;
  animation-duration: 11s;
}

@keyframes animate {
  0% {
    transform: translateY(0) rotate(0deg);
    opacity: 1;
    border-radius: 0;
  }

  100% {
    transform: translateY(-1000px) rotate(720deg);
    opacity: 0;
    border-radius: 50%;
  }
}
/*
-- End BackGround Animation 
*/
</style>
