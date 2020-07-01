<template>
  <div class="avatar">
    <div class="avatar_face">
      <img src="./../assets/face.jpg" alt="">
    </div>
    <h2 class="avatar_name">Hello, Jane.</h2>
    <p class="avatar_tips">
      Looks like feed good<br /> You hava 7 tasks to do today
    </p>
    <p class="avatar_date">TODAY : {{ today | dateString}}</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      today: new Date()
    }
  },
  filters: {
    dateString (val) {
      return val
        .toDateString()
        .toUpperCase()
        .replace(/(\s\d{4})$/, ', $1')
    }
  }
}
</script>

<style lang="scss">
.avatar {
  display: flex;
  flex-direction: column;
  padding: 0 40px;
  justify-content: flex-end;
  height: 300px;
}

.avatar_face {
  width: 44px;
  height: 44px;
  overflow: hidden;
  border-radius: 100%;
  box-shadow: 0 5px 10px rgba(0, 0, 0, .2);

  img {
    width: 100%;
    height: 100%;
  }
}

.avatar_name {
  margin-top: 32px;
  font-size: 32px;
  padding: 0 6px;
  font-weight: 300;
  letter-spacing: 1px;
}

.avatar_tips {
  padding: 0 6px;
  margin-top: 16px;
  font-size: 13px;
  font-weight: 100;
  line-height: 1.6em;
  opacity: .8;
}

.avatar_date {
  margin-top: 44px;
  margin-bottom: 16px;
  padding: 0 6px;
  font-size: 14px;
}
</style>