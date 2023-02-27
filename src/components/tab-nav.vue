
<script>
import TabBar from './tab-bar.vue';
export default {
    name:'TabNav',
    components:{
        TabBar
    },
    render(h) {
        console.log('h :', h);
        const tabs = {}
        const panes = {}
        return (
            <div>
              {<tab-bar tabs={panes}></tab-bar>}
              {tabs}
            </div>
        )
    }
}
</script>

<style>

</style>