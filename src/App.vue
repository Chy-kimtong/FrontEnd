<template>
  <div id="app">
    <!-- This is navigation bar , the original code I don't know from where. but I did it in the below -->
    <div class="ui inverted segment navbar">
      <div class="ui center aligned container">
        <div class="ui large secondary inverted pointing menu compact">
          <!-- Logo RemindUs -->
          <h1 class="logo">RemindUS</h1>

          <!-- search bar -->
          <div class="search-box">
            <input type="text" placeholder="Search.." class="search-bar" />
          </div>
          <router-link to="/tasks" exact class="item">
            <i class="tasks icon"></i> Tasks
          </router-link>
          <router-link to="/tasks/new" class="item">
            <i class="plus circle icon"></i> New
          </router-link>

          <!-- ### it should be the file name to -->
          <router-link to="/###" exact class="item">
            <!-- icon code from boostrap` -->
            <svg
              width="1em"
              height="1em"
              viewBox="0 0 16 16"
              class="bi bi-check"
              fill="currentColor"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M10.97 4.97a.75.75 0 0 1 1.071 1.05l-3.992 4.99a.75.75 0 0 1-1.08.02L4.324 8.384a.75.75 0 1 1 1.06-1.06l2.094 2.093 3.473-4.425a.236.236 0 0 1 .02-.022z"
              /></svg
            >Done
          </router-link>
        </div>
      </div>
    </div>

    <div class="ui text container">
      <div class="ui one column grid">
        <div class="column">
          <router-view />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
};
</script>

<style>
/* the style I add start */
.logo {
  font-family: "Courier New", Courier, monospace;
  font-size: 72px;
  background: -webkit-linear-gradient(#eee, #333);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  padding-top: 4%;
  margin-right: 10%;
}

.search-box .search-bar {
  margin-top: 60%;
  padding: 10px;
  background: rgb(238, 174, 202);
  background: radial-gradient(
    circle,
    rgba(238, 174, 202, 1) 0%,
    rgba(148, 187, 233, 1) 100%
  );
  display: block;
  width: 100%;

  color: #414141;
  font-size: 20px;

  appearance: none;
  border: none;
  outline: none;

  box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.25);
  border-radius: 5px 5px 5px 5px;
  transition: 0.4s;
}
.search-box .search-bar:focus {
  box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.25);
  background-color: rgba(255, 255, 255, 0.75);
  border-radius: 16px 16px 16px 16px;
}
/* the style I add end */
#app > div.navbar {
  margin-bottom: 1.5em;
}
.myFlash {
  width: 250px;
  margin: 10px;
  position: absolute;
  top: 50;
  right: 0;
}
input {
  width: 300px;
}
div.label {
  width: 120px;
}
div.input {
  margin-bottom: 10px;
}
button.ui.button {
  margin-top: 15px;
  display: block;
}
</style>