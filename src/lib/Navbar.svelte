<script>
    import {page} from "$app/stores";
    import {base} from "$app/paths"
</script>
<div>
    did styles break part 2
    <nav>
        <a href="./about" class:active={$page.url.pathname == {base}+"/about"}> about</a>
        <a href="./contact" class:active={$page.url.pathname == {base}+"/contact"}> contact</a>
        <a href="./#" class:active={$page.url.pathname == {base}+"/"}> home</a>
    </nav>
</div>

{$page.url.pathname} 
{base}
<style lang="scss">
    div{
        background: var(--color--primary);
        display: flex;
        justify-content: space-between;
        padding: 15px;
    }
    nav {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    a{
        text-decoration: none;
        color: white;
        padding: 30px;

        &.active {
            color: var(--color--secondary)
        }
    }
</style>