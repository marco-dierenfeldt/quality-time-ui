<template>
    <div class="row">
        <h2>Zu letzt gebuchte Zeiten</h2>
        <table class="table">
            <tr>
                <th>Datum</th>
                <th>Startzeit</th>
                <th>Endzeit</th>
                <th>Beschreibung</th>
                <th></th>
            </tr>
            <tr v-for="(entry, index) in timeEntries">
                <td>{{entry.date}}</td>
                <td>{{entry.begin}}</td>
                <td>{{entry.end}}</td>
                <td>{{entry.description}}</td>
                <td>
                    <button class="btn btn-primary" title="edit"><i class="fas fa-edit"></i></button>&nbsp;
                    <button class="btn btn-danger" title="delete" @click="deleteEntry(index)"><i class="fas fa-times-circle"></i></button>
                </td>
            </tr>
        </table>
    </div>
</template>

<script>
    export default {
        name: "TimeEntryList",
        data() {
            return {
                timeEntries: [
                    {
                        date: '08.05.2019',
                        begin: '7:00',
                        end: '11:30',
                        description: 'Projektarbeit'
                    },
                    {
                        date: '08.05.2019',
                        begin: '12:00',
                        end: '15:30',
                        description: 'Projektarbeit'
                    },
                    {
                        date: '09.05.2019',
                        begin: '7:00',
                        end: '11:30',
                        description: 'Projektarbeit'
                    },
                    {
                        date: '09.05.2019',
                        begin: '12:00',
                        end: '15:30',
                        description: 'Projektarbeit'
                    },
                    {
                        date: '10.05.2019',
                        begin: '7:00',
                        end: '11:30',
                        description: 'Projektarbeit'
                    },
                    {
                        date: '10.05.2019',
                        begin: '12:00',
                        end: '15:30',
                        description: 'Projektarbeit'
                    }
                ]
            }
        },
        methods: {
            deleteEntry(index) {
                this.timeEntries.splice(index, 1);
            }
        }
    }
</script>

<style scoped>

</style>