<template>
    <JqxSplitter :theme="'material'" 
        :width="850" :height="600" :orientation="'horizontal'"
        :panels="[{ size: '50%', collapsible: false }, { size: '50%' }]">
        <div>
            <JqxTabs :theme="'material'" ref="myTabs1" class="jqx-hideborder jqx-hidescrollbars"
                :width="'100%'" :height="'100%'">
                <ul>
                    <li style="margin-left: 30px;">Tab 1</li>
                    <li>Tab 2</li>
                </ul>
                <div>
                    Content 1
                </div>
                <div>
                    Content 2
                </div>
            </JqxTabs>
        </div>
        <div>
            <JqxSplitter :theme="'material'" 
                :width="'100%'" :height="300"
                :panels="[{ size: '50%' }]">
                <div>
                    <JqxTabs :theme="'material'" ref="myTabs2" class="jqx-hideborder jqx-hidescrollbars" 
                        :width="'100%'" :height="'100%'">
                        <ul>
                            <li style="margin-left: 30px;">Tab 1</li>
                            <li>Tab 2</li>
                        </ul>
                        <div>
                            Content 1
                        </div>
                        <div>
                            Content 2
                        </div>
                    </JqxTabs>
                </div>
                <div>
                    <JqxTabs :theme="'material'" ref="myTabs3" class="jqx-hideborder jqx-hidescrollbars"
                        :width="'100%'" :height="'100%'">
                        <ul>
                            <li style="margin-left: 30px;">Tab 1</li>
                            <li>Tab 2</li>
                        </ul>
                        <div>
                            Content 1
                        </div>
                        <div>
                            Content 2
                        </div>
                    </JqxTabs>
                </div>
            </JqxSplitter>
        </div>
    </JqxSplitter>
</template>

<script>
    import JqxSplitter from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxsplitter.vue';
    import JqxTabs from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxtabs.vue';

    export default {
        components: {
            JqxSplitter,
            JqxTabs
        }
    }
</script>

<style>
  
   
</style>