<template>
  <ul class="nav">
    <li class="item"><a class="item-link" href="/">ⒻⒶⓃⒸⓎ</a></li>
    <li class="item">
      <a class="item-link" href="#">
        <div class="dropdown">
          <span>Links</span>
          <div class="dropdown-content">
            <div><a href="#"></a></div>
            <div><a href="#"></a></div>
          </div>
        </div>
      </a>
    </li>
    <li class="item">
      <a class="item-link" href="https://github.com/liaojiaming123/Fancy" target="_blank"><img src="../assets/github.png" alt="github"></a>
    </li>
  </ul>
</template>
<script>
export default {};
</script>
<style scoped>
.nav {
  width: 100%;
  height: 56px;
  background-color: #ffffff00;
  display: flex;
  justify-items: center;
  justify-content: flex-end;
  border-bottom: 1px solid #eef;
}
.item:first-child {
  margin-right: auto;
  font-size: 1.25rem;
  font-weight: bolder;
}
.item:nth-child(2) {
  visibility: hidden;
}
.item {
  list-style: none;
  margin: auto 1em;
}
.item-link {
  text-decoration: none;
  color: lightslategray;
}
.dropdown {
  position: relative;
  display: inline-block;
}
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  padding: 12px 16px;
}
.dropdown:hover .dropdown-content {
  display: block;
}
</style>