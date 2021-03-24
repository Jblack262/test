<template>
    <div class="navbar">
        <ul class="list">
            <li><i @click="openNavbar" :class="{active: isActive}" class="fa fa-plus fa-3x"></i></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
        isActive: false,
        }
    },
    methods: {
        openNavbar() {
            this.isActive = !this.isActive;
        }
    }
}
</script>

<style lang="scss">
    body {
        margin: none;
    }
    .navbar {
        margin: none;
        position: absolute;
        top: 0;
        left: 0;
        width: 100vw;
        background: skyblue;
        ul.list {
            list-style-type: none;
            padding: 0 1rem;
            margin: 0;
            display: flex;
            justify-content: space-between;
                li {
                    width: 100%;
                    color: black;
                    text-decoration: none;
                    display: flex;
                    align-items: center;
                    justify-content: flex-end;
                    cursor: pointer;
                    i {
                        float: right;
                        padding-top: 2px;
                    }
                    .active {
                        transform: rotate(90deg);
                        transition: transform 800ms;
                    }
                }
        }
    }
</style>