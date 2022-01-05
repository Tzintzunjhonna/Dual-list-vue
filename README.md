# Dual-list-vue
![Sin título](https://user-images.githubusercontent.com/57906607/148164414-6033ebbc-fc2d-47ac-b439-540f5e0d4979.png)

# Como instalar

npm install https://github.com/Tzintzunjhonna/Dual-list-vue --save

# Como usar

import DualListBox from "dual-listbox-vue";
import "dual-listbox-vue/dist/dual-listbox.css";
export default {
    name: "App",
    components: {
        DualListBox
    },
    data: function () {
        return {
            source: [
                { name: "WHITE", code: "#FFFFFF" },
                { name: "SILVER", code: "#C0C0C0" },
                { name: "GRAY", code: "#808080" }
            ],
            destination: [
                { name: "BLACK", code: "#000000" },
                { name: "RED", code: "#FF0000" }
            ]
        };
    },
    methods: {
        onChangeList: function ({ source, destination }) {
            this.source = source;
            this.destination = destination;
        }
    }
};

# Template Vue

<DualListBox
    :source="source" 
    :destination="destination"
    label="name"
    @onChangeList="onChangeList"
/>
