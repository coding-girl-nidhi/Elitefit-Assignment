<template>
  <div class="item">
    <img :src="img" alt="s" />
    <p class="name">{{ name }}</p>
    <div id="text">"{{ message }}"</div>
  </div>
</template>

<script>
export default {
  name: "TestimonialCard",
  //   created() {
  //     this.showText();
  //   },
  methods: {},
  props: ["message", "img", "name"],
};
</script>

<style>
.item {
  width: 23%;
  border-radius: 20px;
  position: relative;
  overflow: hidden;
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  cursor: pointer;
}

.item:hover #text {
  display: flex;
}
.item img {
  width: 100%;
}
.item p {
  display: flex;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 36px;
  font-weight: 700;
  line-height: 45px;
  letter-spacing: 0em;
  text-align: center;
  color: #ffffff;
}
.item div {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 15px;
  font-weight: 400;
  line-height: 24px;
  letter-spacing: 0em;
  text-align: left;
  color: #ffffff;
  width: 100%;
  height: 100%;
  z-index: 2;
  background-color: black;
  display: none;
  align-items: center;
  padding: 0px 20px;
}
@media only screen and (max-width: 767px) {
  .item {
    width: 90%;
  }
}
</style>
