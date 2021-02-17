<template>
  <div class="container">
    <h4>
      <b-icon icon="cart"></b-icon>รายการสินค้า<b-icon icon="cart"></b-icon>
    </h4>
    <h1>total Buy = {{ buyClick7 }} บาท</h1>

    <b-button variant="success" > ชำระเงิน </b-button>

    <b-button variant="danger" @click="CancelAllItem">
      ยกเลิกการซื้อทั้งหมด
    </b-button>
    <div>
      <b-card-group deck>
        <b-card
          id:1
          title="Illya"
          img-src="https://resize.cdn.otakumode.com/full/u/45ad53869d004fafb5a16c99a79845a4.jpg"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            50,000 บาท
          </b-card-text>
          <template #footer>
            <small class="text-muted">
              <b-button variant="warning" @click="buyClickI1">
                Buy<b-badge variant="light"
                  >{{ buyClick1
                  }}<span class="sr-only">unread messges</span></b-badge
                >
              </b-button>
              <b-button variant="danger" @click="CancelItem1">
                Cancel
              </b-button></small
            >
          </template>
        </b-card>

        <b-card
          id:2
          title="Fate Canival"
          img-src="https://cdn.animenewsnetwork.com/thumbnails/fit750x750/cms/news.4/168036/w700.jpeg"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            25,000 บาท
          </b-card-text>
          <template #footer>
            <small class="text-muted"
              ><b-button variant="warning" @click="buyClickI2">
                Buy<b-badge variant="light"
                  >{{ buyClick2
                  }}<span class="sr-only">unread messges</span></b-badge
                >
              </b-button>
              <b-button variant="danger" @click="CancelItem2">
                Cancel
              </b-button></small
            >
          </template>
        </b-card>

        <b-card
          id:3
          title="Kimetsu no yaiba"
          img-src="https://i.pinimg.com/736x/31/c0/cf/31c0cf74246eb496720ec91c03049282.jpg"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            1,000 bath
          </b-card-text>
          <template #footer>
            <small class="text-muted"
              ><b-button variant="warning" @click="buyClickI3">
                Buy<b-badge variant="light"
                  >{{ buyClick3 }}<span class="sr-only">unread messges</span>
                </b-badge>
              </b-button>
              <b-button variant="danger" @click="CancelItem3">
                Cancel
              </b-button>
            </small>
          </template>
        </b-card>
      </b-card-group>
    </div>
    <div>
      <b-card-group deck>
        <b-card
          id:4
          title="Arknight Blaze"
          img-src="https://static.displate.com/857x1200/displate/2020-07-06/1daab3cb667d53897fe14fc9cf6109a4_41f3726e0993fb2bde0eeeb347ea47d6.jpg"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            500 บาท
          </b-card-text>
          <template #footer>
            <small class="text-muted"
              ><b-button variant="warning" @click="buyClickI4">
                Buy<b-badge variant="light"
                  >{{ buyClick4
                  }}<span class="sr-only">unread messges</span></b-badge
                >
              </b-button>
              <b-button variant="danger" @click="CancelItem4">
                Cancel
              </b-button></small
            >
          </template>
        </b-card>

        <b-card
          id:5
          title="Peko Peko"
          img-src="https://i.redd.it/nbx10zlydeb51.png"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            5,000 บาท
          </b-card-text>
          <template #footer>
            <small class="text-muted"
              ><b-button variant="warning" @click="buyClickI5">
                Buy<b-badge variant="light"
                  >{{ buyClick5
                  }}<span class="sr-only">unread messges</span></b-badge
                >
              </b-button>
              <b-button variant="danger" @click="CancelItem5">
                Cancel
              </b-button></small
            >
          </template>
        </b-card>
        <b-card
          id:6
          title="The Witcher 3"
          img-src="https://m.media-amazon.com/images/M/MV5BYjY3ODFmNWUtNjhjNC00NTExLWIxYmEtYmQ0YTk5NjkzYTUwXkEyXkFqcGdeQXVyNzEyNjcwNTk@._V1_.jpg"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            100,000 บาท
          </b-card-text>
          <template #footer>
            <small class="text-muted"
              ><b-button variant="warning" @click="buyClickI6">
                Buy<b-badge variant="light"
                  >{{ buyClick6
                  }}<span class="sr-only">unread messges</span></b-badge
                >
              </b-button>
              <b-button variant="danger" @click="CancelItem6">
                Cancel
              </b-button></small
            >
          </template>
        </b-card>
      </b-card-group>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      buyClick1: 0,
      buyClick2: 0,
      buyClick3: 0,
      buyClick4: 0,
      buyClick5: 0,
      buyClick6: 0,
      buyClick7: 0
    };
  },
  methods: {
    buyClickI1() {
      this.buyClick1++;
      this.buyClick7 += 50000;
    },
    buyClickI2() {
      this.buyClick2++;
      this.buyClick7 += 25000;
    },
    buyClickI3() {
      this.buyClick3++;
      this.buyClick7 += 1000;
    },
    buyClickI4() {
      this.buyClick4++;
      this.buyClick7 += 500;
    },
    buyClickI5() {
      this.buyClick5++;
      this.buyClick7 += 5000;
    },
    buyClickI6() {
      this.buyClick6++;
      this.buyClick7 += 100000;
    },
    CancelItem1() {
      if (this.buyClick1 > 0) {
        this.buyClick1--;
        this.buyClick7 -= 50000;
      }
    },
    CancelItem2() {
      if (this.buyClick2 > 0) {
        this.buyClick2--;
        this.buyClick7 -= 25000;
      }
    },
    CancelItem3() {
      if (this.buyClick3 > 0) {
        this.buyClick3--;
        this.buyClick7 -= 1000;
      }
    },
    CancelItem4() {
      if (this.buyClick4 > 0) {
        this.buyClick4--;
        this.buyClick7 -= 500;
      }
    },
    CancelItem5() {
      if (this.buyClick5 > 0) {
        this.buyClick5--;
        this.buyClick7 -= 5000;
      }
    },
    CancelItem6() {
      if (this.buyClick6 > 0) {
        this.buyClick6--;
        this.buyClick7 -= 100000;
      }
    },
    CancelAllItem() {
      if (this.buyClick7 > 0) {
        (this.buyClick1 = 0),
          (this.buyClick2 = 0),
          (this.buyClick3 = 0),
          (this.buyClick4 = 0),
          (this.buyClick5 = 0),
          (this.buyClick6 = 0),
          (this.buyClick7 = 0);
      }
    },
    showList() {
      
    }
  }
};
</script>
