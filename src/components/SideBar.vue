<template>
  <aside id="sidebar">
    <div id="nav-blog" class="sidebar-item">
      <h3>Consumption today</h3>
      <a href="#" class="btn btn-success">See more</a>
    </div>

    <div id="search" class="sidebar-item">
      <h3>New schedulling</h3>
      <p>Write the name of your home appliance</p>
      <form>
        <input type="text" name="search" />
        <input type="submit" name="submit" value="Apply" class="btn" />
      </form>
    </div>
  </aside>
</template>

<script>
export default {
  name: "SideBar",
};
</script>

<style>
</style>