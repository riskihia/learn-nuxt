<template>
  <div>
    <NuxtLayout>
      <header>
        <ul>
          <li>
            <NuxtLink to="/">Home</NuxtLink>
            <NuxtLink to="/event">Event</NuxtLink>
            <NuxtLink to="/events/profile">Profile</NuxtLink>
          </li>
        </ul>
      </header>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
