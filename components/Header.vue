<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarTogglerDemo01"
      aria-controls="navbarTogglerDemo01"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
      <NuxtLink to="/">
        <a class="navbar-brand" href="#">OUR CLUBS</a>
      </NuxtLink>
      <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
        <li class="nav-item active">
            <NuxtLink to='/' class="nav-link">
                Home <span class="sr-only">(current)</span>
            </NuxtLink>
        </li>
        <li class="nav-item active">
            <NuxtLink to='/club_top' class="nav-link">
               Clubs <span class="sr-only">(current)</span>
            </NuxtLink>
        </li>
        <li class="nav-item active">
            <NuxtLink to='/about' class="nav-link">
               About <span class="sr-only">(current)</span>
            </NuxtLink>
        </li>
      </ul>
      <form class="form-inline my-2 my-lg-0">
        <input
          class="form-control mr-sm-2"
          type="search"
          placeholder="Search"
          aria-label="Search"
        />
        <button class="btn btn-outline-success my-2 my-sm-0" type="submit">
          Search
        </button>
      </form>
    </div>
  </nav>
</template>