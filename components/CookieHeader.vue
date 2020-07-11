<template>
    <div class="header-container">
        <div class="cookie-header-wrapper">
            <div class="cookie-header">
                <p>{{headerMessage}}</p>
            </div>
        </div>
        <div class="cookie-icon-wrapper">
            <div class="cookie-icon"></div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        headerMessage: String
    }
}
</script>

<style scoped>
.header-container {
  width: 100vw;
  display: flex;
  flex-direction: column;
}
.cookie-header-wrapper {
  width: 100vw;
  height: 200px;
  margin: 0;
  padding: 0;
  background-image: url('../static/cookie-header.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  z-index: 1;
}

.cookie-header {
  width: 100vw;
  height: 200px;
  margin: 0;
  padding: 0;
  background-color: rgba(0,0,0, 0.7);
  z-index: 3;
  display: flex;
  align-items: center;
  justify-content: center;
}

.cookie-header p {
  color: #fff;
  font-size: 26px;
  text-align: center;
}

.cookie-icon-wrapper {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background: linear-gradient(180deg, #FFFFFF 0%, rgba(255, 255, 255, 0) 100%), #EEEEEE;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  display: flex;
  align-self: center;
  justify-self: center;
  align-items: center;
  justify-content: center;
  margin-top: -50px;
  z-index: 5;
}

.cookie-icon {
  width: 80px;
  height: 80px;
  background-image: url('../static/cookiedev.png');
  background-size: cover;
  background-position: center;
  z-index: 6;
}
</style>