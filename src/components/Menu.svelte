<script lang="ts">
    import {Link} from 'svelte-routing';
</script>

<nav class="hidden text-gray-500 uppercase text-bold sm:block">
    <ul>
        <li><Link to="/">Home</Link></li>
        <li><Link to="about">About</Link></li>
        <li><Link to="contact">Contact</Link></li>
    </ul>
</nav>

<style>
    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        overflow: hidden;
    }

    li {
        float: left;
        padding: 0 25px;
    }

    li a {
        display: block;
        color: white;
        text-align: center;
        padding: 16px;
        text-decoration: none;
    }

    li a:hover {
        color: #808080;
    }

    @media screen and (max-width: 600px) {
        nav {
            display: none;
        }
    }
</style>