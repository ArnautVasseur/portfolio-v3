import { BigPaper } from '../.nuxt/components';
<template>
  <div class="book">

    <div class="cover">

      <div class="binding">
        <binding class="bg"/>
        <img class="knot" src="/public/book/knot.png" alt="knot">
      </div>

      <div class="cover_content">
        <div class="corners">
          <border class="corner-1"/>
          <border class="corner-2"/>
        </div>
        <div class="papers">
          <big-paper :rotation="7" class="paper-1"/>
          <big-paper :rotation="2" class="paper-2"/>
          <small-paper :rotation="-7" class="paper-3"/>
          <small-paper :rotation="-2" class="paper-4"/>
        </div>
        <div class="background">
          <img src="/public/book/pattern_cover.png" alt="cover_book">
          <cover-bg class="bg"/>
        </div>

        <div class="content">
          <book-title/>

          <div class="general_stats">
            <tab class="tab" content="7" label="School Projects"/>
            <tab class="tab" content="2" label="Professionals Projects"/>
            <tab class="tab" content="1" label="Other Projects"/>
          </div>

          <div class="distribution">
            <div class="dots">
              <div class="dot-1 dot"></div>
              <div class="dot-2 dot"></div>
              <div class="dot-3 dot"></div>
              <div class="dot-4 dot"></div>
            </div>
            <div class="category">
              <img class="zoroark" src="/public/pokemon/zoroark.png" alt="zoroark">
                <div class="graph">
                  <div class="front-end">
                    <h3>Front-end</h3>
                    <p>40%</p>
                  </div>
                  <div class="full-stack">
                    <h3>Full Stack</h3>
                    <p>60%</p>
                  </div>
                </div>
              <img class="avalugg" src="/public/pokemon/avalugg.png" alt="avalugg">
            </div>
          </div>

        </div>
      </div>
      
      
    </div>
    
    <div class="page"></div>
    <div class="page"></div>
    <div class="page"></div>
    <div class="page"></div>
  </div>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>

.book{
  width: 1067px;
  height: 650px;
  filter: drop-shadow(0 0 100px rgb(0, 0, 0, 50%));

  .cover{
    width: 100%;
    height: 100%;
    display: flex;
    border-radius: 20px;
    background: transparent;

    .binding{
      position: relative;
      width: 150px;
      height: 100%;
      border-radius: 15px 0px 0px 15px;

      .knot{
        position: absolute;
        left: 0;
        top: 0;
        bottom: 0;
        margin: auto;
        z-index: 3;
        height: 70%;
        transform: translateX(-35%);
      }
    }

    &_content{
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      width: 917px;
      height: 100%;
      border-radius: 0px 15px 15px 0px;

      .corner-1, .corner-2, .paper-1, .paper-2, .paper-3, .paper-4{
        position: absolute;
        margin: auto;
      }

      .corner-1{
        top: -1%;
        right: -1%;
        z-index: 3;
      }

      .corner-2{
        bottom: -1%;
        right: -1%;
        z-index: 3;
        transform: rotate(90deg);
      }

      .paper-1{
        top: 65%;
        right: -8%;
      }

      .paper-2{
        top: 55%;
        right: -8%;
      }

      .paper-3{
        top: 15%;
        right: -6%;
      }

      .paper-4{
        top: 25%;
        right: -6%;
      }

      .background{
        position: absolute;
        width: 100%;
        height: 100%;
        overflow: hidden;

        img, .bg{
          position: absolute;
          top: 0;
          right: 0;
          left: 0;
          bottom: 0;
          margin: auto;
        }



        img{
          transform: translateX(-20%);
          z-index: 1;
        }

        .bg{
          z-index: 2;
        }
      }

      .content{
        z-index: 5;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
        width: 100%;
        height: 100%;

        .general_stats{
          display: flex;
          justify-content: space-evenly;
          align-items: center;
          width: 100%;

          .tab{
            z-index: 10;
          }
        }

        .distribution{
          position: relative;
          display: flex;
          justify-content: space-around;
          align-items: center;
          width: 85%;
          height: 150px;
          background: $primary-300;
          border-radius: 10px;
          filter: drop-shadow(0px 0px 40px rgb(0, 0, 0, 20%));

          .dots{
            position: absolute;
            width: 100%;
            height: 100%;

            .dot{
              position: absolute;
              margin: auto;
              background: $background-200;
              border-radius: 50%;
              width: 10px;
              height: 10px;
            }

            .dot-1{
              top: 12%;
              left: 2.5%;
            }

            .dot-2{
              top: 12%;
              right: 2.5%;
            }

            .dot-3{
              bottom: 12%;
              right: 2.5%;
            }

            .dot-4{
              bottom: 12%;
              left: 2.5%;
            }
          }

          .category{
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: space-around;
            align-items: center;

            .graph{
              width: 70%;
              height: 60%;
              display: flex;

              .front-end{
                width: 40%;
                height: 100%;
                background: $background-200;
                box-shadow: inset 0 0 0 5px #E15E61,
                            inset 0 0 0 10px #ED9B99;
                padding: 20px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                color: #E15E61;

                h3{
                  font-size: 1.5rem;
                  font-family: $Sen;
                }

                p{
                  font-size: 2.2rem;
                  font-weight: 500;
                  font-family: $KyoMadoka;
                }
              }

              .full-stack{
                width: 60%;
                height: 100%;
                background: $background-200;
                box-shadow: inset 0 0 0 5px #434E7C,
                            inset 0 0 0 10px #AEB7F2;
                  padding: 20px;
                display: flex;
                justify-content: space-around;
                align-items: center;
                color: #434E7C;

                h3{
                  font-size: 1.5rem;
                  font-family: $Sen;
                }

                p{
                  font-size: 2.2rem;
                  font-weight: 500;
                  font-family: $KyoMadoka;
                }
              }
            }

            img{
              position: absolute;
              margin: auto;
            }

            .zoroark{
              top: 0;
              bottom: 0;
              left: 5%;
              width: 13%;
            }

            .avalugg{
              bottom: 20%;
              right: 4%;
              width: 17%;
            }
          }
        }

        .distribution::before{
          content: "";
          position: absolute;
          width: calc(100% - 20px);
          height: calc(100% - 20px);
          border: 2px solid $background-200;
        }

      }
    }
  }
}

</style>