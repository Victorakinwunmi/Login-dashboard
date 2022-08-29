<template>
  <div class="block lg:flex">
    <SidebarContainer>
      <template #hamburgermenuopen>
        <button class="">
          <img :src="require('@/assets/icons/Menu.png')" class="w-8 m-0 p-0" />
        </button>
      </template>

      <template #hamburgermenuclose>
        <button class="">
          <img :src="require('@/assets/icons/Close.png')" class="w-8 m-0 p-0" />
        </button>
      </template>

      <template #logo>
        <SidebarLogo />
      </template>

      <template #menu>
        <SidebarMenu path="./dashboard">
          <div><SharedIcons icon_name="icon1" /></div>
          <div>Home</div>
        </SidebarMenu>

        <SidebarMenu path="./classes">
          <div><SharedIcons icon_name="icon2" /></div>
          <div>Classes</div>
        </SidebarMenu>

        <SidebarMenu path="./payments">
          <div><SharedIcons icon_name="icon3" /></div>
          <div>Payments</div>
        </SidebarMenu>

        <SidebarMenu path="./tools">
          <div><SharedIcons icon_name="icon4" /></div>
          <div>Tools</div>
        </SidebarMenu>
      </template>

      <template #logout>
        <div><SidebarLogout /></div>
      </template>
    </SidebarContainer>

    <div class="w-full p-6 lg:px-32 xl:px-40">
        <ClassesWelcomeText/>
    </div>
  </div>
</template>

<script>
export default {

};
</script>

<style>
</style>