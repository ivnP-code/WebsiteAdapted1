<template>
  <div class="nav-container">
    <div class="sidebar" :class="{ open: isOpen }">
      <input class="textbar" placeholder="Поиск" />
      <div class="Topline2">МЕНЮ</div>
      <ul class="menu">
        <li>Главная</li>
        <li>Про нас</li>
        <li>Контакты</li>
      </ul>

      <div class="Topline2">ИНФОРМАЦИЯ</div>
      <div class="extra-text">
        <div class="wrap">
          <img src="/images/corpopeople.jpg" class="menupic" />
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi
            autem officia officiis vero illo quam dolore atque molestiae velit
            quia...
          </p>
        </div>
        <div class="wrap">
          <img src="/images/screen.jpg" class="menupic" />
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi
            autem officia officiis vero illo quam dolore atque...
          </p>
        </div>
          <button class="Readmore">ДАЛЕЕ</button>
      </div>

      <div class="Topline3">ПОМОЩЬ</div>
      <p class="help-text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi
        autem officia officiis vero illo quam dolore atque molestiae velit
        quia...
      </p>

      <ul class="contact-list">
        <li>
          <img src="/images/mail.jpg" alt="email icon" />
          <span>druzhba@gmail.com</span>
        </li>
        <li>
          <img src="/images/phone.png" alt="phone icon" />
          <span>0-000-000</span>
        </li>
        <li>
          <img src="/images/house.png" alt="address icon" />
          <span>USA Washington Seatle Northway 1222</span>
        </li>
        <br>
        <br>
      </ul>
    </div>

    <div class="content-wrapper" :class="{ shifted: isOpen }">
      <div class="TopButton" @click="toggleMenu">
        <img src="/images/list-search.png" alt="toggle menu" />
      </div>
      <div class="Topline">СМИ портал</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>

<style scoped>
.nav-container {
  overflow-x: hidden;
}

.sidebar {
  position: fixed;
  top: 0;
  left: -440px;
  width: 250px;
  height: 100vh;
  background: #fff;
  box-shadow: 4px 0 12px rgba(0, 0, 0, 0.15);
  transition: left 0.3s ease;
  z-index: 1000;
  overflow-y: auto;
  padding: 20px;
}
.sidebar.open {
  left: 0;
}

.content-wrapper {
  transition: transform 0.3s ease;
}
.content-wrapper.shifted {
  transform: translateX(250px);
}

.TopButton {
  margin: 20px;
  width: 50px;
  height: 50px;
  cursor: pointer;
}
.TopButton img {
  width: 100%;
  height: 100%;
}

.Topline {
  padding-bottom: 20px;
  border-bottom: 4px solid rgb(22, 108, 206);
  font-weight: 700;
  font-size: 24px;
  margin: 0 80px 20px;
}

.Topline2 {
  margin-top: 20px;
  padding-bottom: 10px;
  border-bottom: 2px solid rgb(22, 108, 206);
  font-weight: 700;
  font-size: 20px;
}

.Topline3 {
  margin-top: 20px;
  padding-bottom: 10px;
  border-bottom: 2px solid rgb(22, 108, 206);
  font-weight: 700;
  font-size: 20px;
}

.textbar {
  padding: 8px;
  margin-bottom: 20px;
  border: 2px solid gray;
  border-radius: 6px;
  font-weight: 700;
  color: gray;
}

.menu {
  list-style: none;
  padding: 0;
  margin: 0 0 20px;
}
.menu li {
  font-size: 18px;
  margin-bottom: 15px;
  cursor: pointer;
}

.extra-text .wrap {
  gap: 10px;
  margin-bottom: 20px;
}
.menupic {
  margin-top: 20px ;
  width: 200px;
  max-height: 150px;
  border-radius: 4px;
}

.Readmore {
  padding: 8px 12px;
  border: 2px solid rgb(92, 184, 214);
  border-radius: 6px;
  background-color: white;
  color: rgb(92, 184, 214);
  font-weight: 700;
  cursor: pointer;
  transition: background-color 0.3s ease;
  margin-top: 10px;
}
.Readmore:hover {
  background-color: rgb(206, 213, 225);
}

.help-text {
  font-size: 14px;
  margin-bottom: 20px;
}

.contact-list {
  list-style: none;
  padding: 0;
  margin: 0;
}
.contact-list li {
  display: flex;
  align-items: center;
  margin-bottom: 12px;
  font-size: 16px;
}
.contact-list li img {
  width: 20px;
  height: 20px;
  margin-right: 8px;
  flex-shrink: 0;
}
</style>
