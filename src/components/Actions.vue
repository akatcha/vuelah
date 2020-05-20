<template>
    <div class="fixed-bottom">
        <b-container class="actions-container">
            <b-row class="actions-row">
                <b-col class="action-column">
                    <Action
                        title="Sailing"
                        type="sailing"
                        svgURL="https://image.flaticon.com/icons/svg/464/464687.svg"
                    />
                </b-col>
                <b-col class="action-column">
                    <Action
                        title="History"
                        type="history"
                        svgURL="https://image.flaticon.com/icons/svg/2224/2224395.svg"
                    />
                </b-col>
                <b-col class="action-column">
                    <Action
                        title="Homes"
                        type="realEstate"
                        svgURL="https://image.flaticon.com/icons/svg/684/684834.svg"
                    />
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>
<script>
import Action from "./Actions";

export default {
    name: "Actions",
    components: {
        Action,
    },
};
</script>
<style scoped>
.actions-container {
    display: flex;
    justify-content: center;
    padding-top: 591.44px / 1127.34px * 100%;
    position: relative;
    bottom: 1rem;
}

.actions-row {
    justify-content: center;
    width: 100vw;
}

.action-column {
    padding-left: 1vw;
    padding-right: 1vw;
}
</style>
