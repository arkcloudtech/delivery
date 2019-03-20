<template>
        <div>
            <h2>Puffy Driver Map</h2>
            <slot></slot>
        </div>
</template>


<script>
export default {
    name: 'PuffyMap',
    data: function(){
        return {
            name: 'Puffy Delivery Map',
            activeTab: 0,
            tabs: [
                { id: 0, title: 'Driver Map', desc: 'show updated driver locations' },
                { id: 1, title: 'Driver Listing', desc: 'list of drivers' },
                { id: 2, title: 'Customer Map', desc: 'show updated customer locations' },
                { id: 3, title: 'Customer Listing', desc: 'list of customers' },
                { id: 4, title: 'Active Orders', desc: 'show orders in transit' }
            ]
        }
    },
    methods: {
        loadPuffyMap: function(){},
        getDriverLocations: function(){},
        setDriverLocations: function(){},
        getCoverageAreas: function(){ 
            return {
                polyRegions: [
                    { 
                        name : "SoCal 1", 
                        desc: "",
                        verts: [
                            { lat: "33.676740", lon: "-118.021160" },
                            { lat: "33.676740", lon: "-118.021160" },
                            { lat: "33.676740", lon: "-118.021160" },
                            { lat: "33.676740", lon: "-118.021160" }
                        ],
                        schedule:{}
                    },
                ],
                radiusOrigins: [
                    { 
                        name: "Hub 1", 
                        origin: { lat: "33.676740", lon: "-118.021160" },
                        schedule:{}
                    }
                ]
            }
        }
    }
};
</script>

<style scoped>
    #puffy-map{
        background-color: pink;
    }
</style>