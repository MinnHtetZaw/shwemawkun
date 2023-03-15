<script>
import SummerClassFee from '@/components/Fees/SummerClassFee.vue';
import WeekdayClassFee from '@/components/Fees/WeekdayClassFee.vue';
import WeekendClassFee from '@/components/Fees/WeekendClassFee.vue';
export default {
    components: {
        SummerClassFee,
        WeekdayClassFee,
        WeekendClassFee
    },
    data() {
        return {
            activeFee: 'SummerClassFee',
            fees: [
                { name: 'weekday class', component: 'WeekdayClassFee' },
                { name: 'weekend class', component: 'WeekendClassFee' },
                { name: 'summer class', component: 'SummerClassFee' }
            ]
        }
    },
    computed: {
        lastFee() {
            return this.fees.length - 1
        }
    }
}
</script>
<template>
    <div>
        <div class="container my-5">
            <div class="text-start">
                <div class="upperbar">
                    <div class="row mb-3 gx-5">
                        <div class="col-4">
                            <div class="title">
                                <h4>2022-2023</h4>
                                <h4 class="text-uppercase">school fees</h4>
                            </div>
                        </div>
                        <div class="col-8">
                            <div class="classes d-flex align-items-center">
                                <template v-for="fee, index in fees" :key="fee.name">
                                    <button @click="activeFee = fee.component" class="btn class text-uppercase"
                                        :class="{ 'point-out': fee.component === activeFee }">
                                        {{ fee.name }}
                                    </button>
                                    <div v-if="+index !== lastFee" class="vl"></div>
                                </template>
                            </div>
                        </div>
                    </div>
                </div>
                <component :is="activeFee"></component>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.title {
    color: var(--cus-primary);

    h4 {
        font-weight: bold;
    }
}

.classes {
    margin-left: 100px;

    .class {
        font-size: 20px;
        border-radius: 0;
        font-weight: var(--cus-fw-semibold);
        padding-right: 15px;
    }
}

.point-out {
    background-color: var(--cus-primary);
    color: var(--cus-white);
    border-radius: 15px !important;
}

.vl {
    border-left: 3px solid var(--cus-dark);
    height: 40px;
    margin: 0 1rem;
}
</style>