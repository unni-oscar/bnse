<template>
    <div>
        Unnikrishnan
        <trading-vue :data="chart" :color-back="colors.colorBack"
    :color-grid="colors.colorGrid"
    :color-text="colors.colorText" :overlays="overlays"></trading-vue>

    </div>
</template>
 
<script>
import TradingVue from 'trading-vue-js'
import Data from './data.json'
import Grin from './Grin.js'
    export default {
        name: 'app',
        
        components: { TradingVue },
        data() {
            return {
                chart: Data,
                colors: {
                colorBack: '#fff',
                colorGrid: '#eee',
                colorText: '#333',
            },
            overlays: [Grin],
                ohlcv: [
                    [ 1551128400000, 33,  37.1, 14,  14,  196 ],
                    [ 1551132000000, 13.7, 30, 6.6,  30,  206 ],
                    [ 1551135600000, 29.9, 33, 21.3, 21.8, 74 ],
                    [ 1551139200000, 21.7, 25.9, 18, 24,  140 ],
                    [ 1551142800000, 24.1, 24.1, 24, 24.1, 29 ],
                ]
            }
        }
    }
</script>