<template>
    <JqxScheduler :theme="'material'" ref="myScheduler"
        :width="getWidth" :height="600" :source="dataAdapter" :date="date"  :view="'weekView'" :showLegend="true"
        :appointmentDataFields="appointmentDataFields" :views="views" 
    />
</template>

<script>
    import JqxScheduler from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxscheduler.vue'

    export default {
        components: {
            JqxScheduler
        },
        data: function () {
            return {
				getWidth: '90%',
                date: new jqx.date(2016, 11, 23),
                appointmentDataFields: 
                {
                    from: 'start',
                    to: 'end',
                    id: 'id',
                    description: 'about',
                    location: 'address',
                    subject: 'name',
                    style: 'style',
                    status: 'status'
                },
                views:
                [        
                    { type: 'dayView', showWeekends: true, timeRuler: { scaleStartHour: 7, scaleEndHour: 21 } },
                    { type: 'weekView', showWeekends: true, timeRuler: { scaleStartHour: 7, scaleEndHour: 21 } },
                    { type: 'timelineDayView', showWeekends: true, timeRuler: { scaleStartHour: 7, scaleEndHour: 21 } },
                    { type: 'timelineWeekView', showWeekends: true, timeRuler: { scaleStartHour: 7, scaleEndHour: 21 } }
                ]
            }
        },
        beforeCreate: function () {
            this.source =
                {
                    dataType: 'json',
                    dataFields: [
                        { name: 'id', type: 'string' },
                        { name: 'status', type: 'string' },
                        { name: 'about', type: 'string' },
                        { name: 'address', type: 'string' },
                        { name: 'company', type: 'string' },
                        { name: 'name', type: 'string' },
                        { name: 'style', type: 'string' },
                        { name: 'calendar', type: 'string' },
                        { name: 'start', type: 'date', format: 'yyyy-MM-dd HH:mm' },
                        { name: 'end', type: 'date', format: 'yyyy-MM-dd HH:mm' }
                    ],
                    id: 'id',
                    url: 'appointments.txt'
                };

            this.dataAdapter = new jqx.dataAdapter(this.source);
        }
    }
</script>

<style>
  
   
</style>