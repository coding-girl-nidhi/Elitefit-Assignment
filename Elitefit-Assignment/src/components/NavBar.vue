<template>
  <div id="parentNavbar">
    <div class="freeShipping">FREE SHIPING ON ALL ORDERS</div>
    <div id="navbar">
      <h2>PISTONS</h2>
      <div id="navbarSections">
        <h6>NEW</h6>
        <h6>BRANDS</h6>
        <h6>COLLECTIONS</h6>
        <h6>ACCESSORIES</h6>
        <h6><a href="#about">ABOUT</a></h6>
      </div>
      <div>
        <i class="bi bi-cart3"></i>
        <i @click="openSearchModal" class="bi bi-search"></i>
        <i @click="openMenuBox" id="hamburgerIcon" class="bi bi-list"></i>
      </div>
      <div id="searchModal">
        <div>
          <i @click="closeSearchModal" class="bi bi-x-lg"></i>
        </div>
        <div>
          <input type="text" />
          <button>SEARCH</button>
        </div>
      </div>
      <div id="menuBox">
        <div>
          <i @click="closeMenuBox" class="bi bi-x-lg"></i>
        </div>
        <div>
          <p>NEW</p>
          <p>BRANDS</p>
          <p>COLLECTIONS</p>
          <p>ACCESSORIES</p>
          <p><a href="#about">ABOUT</a></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "bootstrap-icons/font/bootstrap-icons.css";
export default {
  name: "NavBar",
  methods: {
    closeSearchModal() {
      document.getElementById("searchModal").style.display = "none";
    },
    openSearchModal() {
      document.getElementById("searchModal").style.display = "block";
    },
    closeMenuBox() {
      document.getElementById("menuBox").style.display = "none";
    },
    openMenuBox() {
      document.getElementById("menuBox").style.display = "block";
    },
  },
};
</script>

<style>
#parentNavbar {
  position: fixed;
  top: 0;
  z-index: 1000;
}
.freeShipping {
  width: 100vw;
  text-align: center;
  height: 6vh;
  padding-top: 1vh;
  background-color: #e3e3e3;
}
#navbar {
  display: flex;
  padding: 0px 30px 0px 20px;
  height: 14vh;
  align-items: center;
  justify-content: space-between;
  position: relative;
  background-color: white;
}
#navbar > :nth-child(1) {
}
#navbarSections {
  display: flex;
  justify-content: space-around;
  width: 40%;
  align-items: center;
}
#navbar > :nth-child(3) {
  position: relative;
  display: flex;
  justify-content: space-around;
  gap: 15px;
  font-size: 24px;
  align-items: center;
}
#hamburgerIcon {
  display: none;
}
#searchModal {
  display: none;
  width: 25vw;
  background-color: white;
  position: absolute;
  right: 15px;
  top: 0;
  transition-duration: 20ms;
}
#searchModal > :nth-child(1) {
  padding: 0px 10px;
  text-align: end;
}
#searchModal > :nth-child(2) {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#searchModal > :nth-child(2) > :nth-child(1) {
  border-radius: 50px;
  width: 65%;
  height: 33px;
  border: solid 1px;
}
#searchModal > :nth-child(2) > :nth-child(2) {
  border-radius: 50px;
  width: 30%;
  font-size: 16px;
  background-color: #000000;
  border: solid #ffecc1 3px;
  color: white;
  height: 41px;
}
#menuBox {
  display: none;
}

/*Small Screen*/
@media only screen and (max-width: 767px) {
  #menuBox {
    display: none;
    width: 60vw;
    position: absolute;
    right: 0;
    top: 0;
    background-color: white;
    padding: 20px;
  }
  #menuBox > :nth-child(1) {
    text-align: end;
  }
  #menuBox > :nth-child(2) {
    display: flex;
    flex-direction: column;
    gap: 28px;
  }
  #menuBox > :nth-child(2) > p {
    font-size: 15px;
    font-weight: 700;
    line-height: 19px;
    letter-spacing: 0em;
  }
  #hamburgerIcon {
    display: block;
  }
  #navbarSections {
    display: none;
  }
  #searchModal > :nth-child(2) > :nth-child(2) {
  }
}
</style>
