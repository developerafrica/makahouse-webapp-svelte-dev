<script>
    import Carousel from "svelte-carousel";
    import { createEventDispatcher } from "svelte";

    let dispatch = createEventDispatcher();

    function rLater(){
        dispatch("popend", true)
    }
</script>

<article >
    <div class="art">
        <div class="cards">
            <div class="cd">
            <Carousel 
            arrows={false}
            infinite={false}
            >

                <div class="pp-cd-one">
                    <div class="ppcd">
                        <header>
                            <div class="hd">
                                <div class="brand">
                                    <h1>makashouse.com</h1>
                                    <p>paize</p>
                                </div>
                            </div>
                        </header>
                        <main>
                            <div class="mn">
                                <h1>makahouse art platform</h1>
                                <hr>
                                <p>welcome to makas house</p>
                                <br>
                                <p>Malawi’s creative realm, Join us as we become Africa’s top entertainment and market platform </p>
                            </div>
                        </main>
                    </div>
                </div>
                <div class="pp-cd-two">
                    <div class="ppcd">
                        <header>
                            <div class="hd">
                                <div class="brand">
                                    <h1>what is this all about ? 😅</h1>
                                    <hr>
                                    <p>paize</p>
                                </div>
                            </div>
                        </header>
                    </div>
                </div>
                
            </Carousel>
                <main>
                    <div class="mn">
                        <button ><p>sign up</p></button>
                        <button on:click={rLater} ><p>remind me later</p></button>
                        <button>
                            <p>&copy makahouse | 2022 <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g data-name="Layer 2"><g data-name="home"><rect width="24" height="24" opacity="0"/><path d="M20.42 10.18L12.71 2.3a1 1 0 0 0-1.42 0l-7.71 7.89A2 2 0 0 0 3 11.62V20a2 2 0 0 0 1.89 2h14.22A2 2 0 0 0 21 20v-8.38a2.07 2.07 0 0 0-.58-1.44zM10 20v-6h4v6zm9 0h-3v-7a1 1 0 0 0-1-1H9a1 1 0 0 0-1 1v7H5v-8.42l7-7.15 7 7.19z"/></g></g></svg> </p>
                        </button>

                    </div>
                </main>


            </div>
        </div>
    </div>
</article>
<style lang="scss">
    @import "../_config.scss";

    article{
        background: var(--we);
        min-height: 100vh;
        position: fixed;
        z-index: 80;
        top: 0;
        left: 0;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        .art{
            width: 100%;

            .cards{
                .cd{
                    .pp-cd-one{
                        .ppcd{
                            header{
                                .hd{
                                    .brand{
                                        background: black;
                                        padding-top: 20vh;
                                        border-radius: 5px;
                                        margin: 20px;
                                        box-shadow: rgba(0, 0, 0, 0.264) 0 0 6px 2px;
                                        h1{
                                            @include font(var(--we), 1.3rem, 500);
                                            padding: 15px;
                                            letter-spacing: 1.2px;
                                        }
                                        p{
                                            @include font(var(--gd), 0.8rem, 600);
                                            padding: 15px;

                                        }
                                        

                                    }
                                }
                            }
                            main{
                                .mn{
                                    padding: 20px;
                                    h1{
                                        @include font(var(--tc),1.2rem, 600);
                                        padding: 10px 0;
                                        
                                    }
                                    p{
                                        @include font(hsl(205, 100%, 19%),1rem, 500);
                                        padding: 10px 0;
                                        
                                    }
                                }
                            }
                        }
                    }
                    main{
                        .mn{
                            width: 100%;
                            button{
                                border: none;
                                text-align: center;
                                background: none;
                                margin: 10px 0;
                                display: flex;
                                flex-direction: column;
                                width: 100%;
                                padding: 5px;
                                p{
                                    @include font(var(--tc), 1rem, 600);
                                    text-transform: uppercase;
                                    padding: 20px 0;
                                    border-radius: 5px;
                                    width: 100%;
                                    display: flex;
                                    justify-content: center;
                                    align-items: center;
                                    svg{
                                        width: 20px;
                                        margin: 0 10px;
                                        filter: grayscale(80);
                                    }

                                }
                                
                            }
                            button:nth-child(1){
                                p{
                                    border: var(--gd) solid 1px;
                                }
                            }
                            button:nth-child(2){
                                p{
                                    background: var(--gd);
                                    &:hover{
                                        background: var(--bl);
                                        color: var(--we);

                                    }
                                }
                            }
                            
                        }
                    }
                    .pp-cd-two{
                        .ppcd{
                            header{
                                .hd{
                                    .brand{
                                        padding: 20px;
                                        h1{
                                            filter: grayscale(50%);
                                            @include font(var(--tc), 1rem, 500);
                                            text-align: center;
                                            padding:20px  10px;
                                        }
                                    }
                                }
                            }

                        }
                    }
                }
            }
        }
        

    }
</style>