<template>
<div>
    <p class="primary-links">
        <a href="#">About Us</a>
        <a href="#">Privacy policy</a>
        <a href="#">Help Center</a>
    </p>
    <p class="secondary-links">
        <a href="#">Terms</a>
        <a href="#">Apps</a>
        <a href="#">Blog</a>
        <a href="#">Status</a>
        <a href="#">Marketing</a>
        <a href="#">Developers</a>
        <a href="#">Plans</a>
        <a href="#">Promotions</a>
        <a href="#">Join Us</a>
    </p>

    <div class="bottom-part">
        <p>Addr: South China University Of Technology</p>
        <p>Email: contact@muses.net</p>
        <p>© 2018 Muses Team</p>
    </div>
</div>
</template>

<style>
.primary-links {
    margin-top: 2em;
    display: flex;
    justify-content: space-between;
}

.secondary-links {
    margin-top: .5em;
    display: flex;
    justify-content: flex-start;
    flex-wrap: wrap;
}

.secondary-links > a {
    padding-right: 1.5em;
}

.primary-links > a, .secondary-links > a  {
    color: rgba(0,0,0,0.54);
    text-decoration: none;
}

.primary-links > a:hover, .secondary-links > a:hover {
    text-decoration: underline;
}

.bottom-part > p {
    color: rgba(0,0,0,0.54);
    margin-bottom: .5em;
}
</style>
