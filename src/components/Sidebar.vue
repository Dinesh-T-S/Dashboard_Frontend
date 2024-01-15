<template>
	<aside :class="`${is_expanded ? 'is-expanded' : ''}`">
		
        <nav class=" logo navbar navbar-light">
            <a class="navbar-brand dec" href="#">
                <img src="../assets/blue.png" alt="Vue" /> 
                Blue Receipt
            </a>
        </nav>

		<div class="menu-toggle-wrap">
			<button class="menu-toggle" @click="ToggleMenu" >
                    <span class="material-icons  ">menu</span>

			</button>
		</div>


        <!-- <h3>Menu</h3> -->
        <div class="menu">
                <form role="form">
                        <div class="form-group" style="padding: 10px;">
                        <input type="text" class="form-control empty" id="iconified" placeholder="&#xF002;" />
                        </div>
                </form>
                <br>
            
            <router-link class="button" to="/home">
                <span class="material-icons">
                    dashboard
                </span>
                <span class="text">
                    Dashboard
                </span>
            </router-link>
            <hr>

            <router-link to="/about" class="button">
				<span class="material-icons">sms</span>
				<span class="text side-title">Conversation</span>
			</router-link>
			<router-link to="/Automation" class="button">
				<span class="material-icons">tune</span>
				<span class="text">Automation</span>
			</router-link>
			<router-link to="/Campigns" class="button">
				<span class="material-icons">bar_chart</span>
				<span class="text">Campigns</span>
			</router-link>
			<router-link to="/popup" class="button">
				<span class="material-icons">forum</span>
				<span class="text">Popup</span>
			</router-link>
			<router-link to="/livechat" class="button">
				<span class="material-icons">chat</span>
				<span class="text">Live Chat</span>
			</router-link>
			<router-link to="/segments" class="button">
				<span class="material-icons">circle</span>
				<span class="text">Segments</span>
			</router-link>
			<router-link to="/integration" class="button">
				<span class="material-icons">integration_instructions</span>
				<span class="text">Integration</span>
			</router-link>
            <router-link to="/bottom" >
                <div class="rounded-top text-black d-flex flex-row" >
                    <div class="ms-4 mt-2 d-flex flex-column">
                        <img src="../assets/face.png" id="bottomMenu">
                    </div>
                    <div id="bottomMenu2">
                        <h6>Dinesh</h6>
                        <p>Store Name</p>
                    </div>
                </div>
			</router-link>
            

        </div>
        

    </aside>
   
</template>

<script setup>
import { ref } from 'vue'


const is_expanded = ref(localStorage.getItem("is_expanded") === "true")

const ToggleMenu = () => {
	is_expanded.value = !is_expanded.value
	localStorage.setItem("is_expanded", is_expanded.value)
}
</script>

<style lang="scss" scoped>
aside {
	display:flex;
	flex-direction: column;

	background-color: var(--lightblue);
	color: var(--dark);

	width: calc(2rem + 32px);
	overflow:hidden;
	min-height: 140vh;
	padding: 01rem;

	transition: 0.2s ease-in-out;

	.flex {
		flex: 1 1 0%;
	}

	.logo {
		margin-top: 0rem;
		img {
			width: 2.6rem;
			border-radius: 100%;

		}
	}

	

	
    .dec{
        text-decoration: none;
        color: dark;
    }
    .empty {
            font-family: FontAwesome;
            font-style: normal;
            font-weight: 400;
            text-decoration: inherit;
            padding: 10px;
            font-size: 18px;
            line-height:10px;
            border:1px solid #ddd;
            border-radius:25px;
			background-color: rgb(217, 232, 245);

  
    }

    #bottomMenu{
    width: 70px;
    height: 70px;
    border-radius: 100%;
    margin-top:16rem;
	margin-left: -20px;
    padding:10px; 
    }
	
    #bottomMenu2{
    margin-top: 16.5em;
    padding: 10px;
	text-decoration: none;

    }

	.menu-toggle-wrap {
		display: flex;
		justify-content: flex-end;
		margin-bottom: -1rem;


		position: fixed;
		top: 0;
		transition: 0.2s ease-in-out;

		.menu-toggle {
			transition: 0.2s ease-in-out;
			.material-icons {
				font-size: 2rem;
				color: var(--dark);
				transition: 0.2s ease-out;
			}
			
			&:hover {
				.material-icons {
					color:  #4dd2ff;
					transform: translateX(0.5rem);
				}
			}
		}
	}

	h3, .button .text {
		opacity: 0;
		transition: opacity 0.3s ease-in-out;
		
	}

	h3 {
		color: var(--grey);
		font-size: 0.875rem;
		margin-bottom: 0.5rem;
		text-transform: uppercase;
	}

	.menu {
		margin: 0 -1rem;
		


		.button {
			display: flex;
			align-items: center;
			text-decoration: none;

			transition: 0.2s ease-in-out;
			padding: 0.5rem 1rem;

			.material-icons {
				font-size: 2rem;
				color: var(--dark);
				transition: 0.2s ease-in-out;
			}
			.text {
				color: var(--dark);
				transition: 0.2s ease-in-out;
			}

			&:hover {
				background-color:  #ccf2ff;
				border-radius:40px;

				.material-icons, .text {
					color: var(--dark);
				}
			}

			&.router-link-exact-active {
				background-color: #4dd2ff;
				border-right: 5px solid var(--light);

				.material-icons, .text {
					color: var(--dark);
				}
			}
		}
	}

	.footer {
		opacity: 0;
		transition: opacity 0.3s ease-in-out;

		p {
			font-size: 0.875rem;
			color: var(--grey);
		}
	}

	&.is-expanded {
		width: var(--sidebar-width);

		.menu-toggle-wrap {
			top: -3rem;
			
			.menu-toggle {
				transform: rotate(-180deg);
                
			}
		}

		h3, .button .text {
			opacity: 1;
		}

		.button {
			.material-icons {
				margin-right: 1rem;
			}
		}

		.footer {
			opacity: 0;
		}
	}

	@media screen and (max-width: 1024px) {
		position: relative;
		z-index:99;
        background-color:var(--dark);

        .dec{
            color: var(--light);
        }

		#bottomMenu2{
			color:white;
		}

        .menu-toggle-wrap {
		

		.menu-toggle {
			.material-icons {
                color: var(--light);

            }
        }
        }

        .menu {

                .button {
                    .material-icons {
                        color: var(--light);
                    }
                    .text {
                        color: var(--light);
                    }
                    
                }
            }

	#bottomMenu{
   
    margin-top:67rem;
	
    }
    #bottomMenu2{
    margin-top: 67em;

    }
	
        
	}


	
}
</style>
