<template>
    <div>
        <div>
		<nav class="navbar navbar-expand-md navbar-light" id="navbar-container">
            <div class="container-fluid">
                <a href="#" class="navbar-brand" id="navbar-name">sunnyside</a>
                <button type="button" v-popover:foo
                    class="navbar-toggler"
                    data-bs-toggle="collapse"
                    data-bs-target="#MenuNavegacion">
                        <svg xmlns="http://www.w3.org/2000/svg" width="26" height="26" fill="currentColor" class="bi bi-list" viewBox="0 0 16 16">
                        <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
                        </svg>
                </button>

                <popover name="foo" class="popover">
                    <ul class="navbar-nav ms-3">
                        <li class="nav-item">
                            <a class="nav-link about" href="#" >About</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link services" href="#" >Services</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link projects" href="#" >Projects</a>
                        </li>
                    </ul>
                    <ul class="navbar-nav ms-3">
                        <li class="nav-item">
                            <a class="nav-link contact" href="#" >CONTACT</a>
                        </li>
                    </ul>
                </popover>
            </div>
			<div id="MenuNavegacion" class="collapse navbar-collapse">
				<ul class="navbar-nav ms-3">
					<li class="nav-item">
                        <a class="nav-link active" href="#" id="menu-about">About</a>
                    </li>
					<li class="nav-item">
                        <a class="nav-link" href="#" id="menu-services">Services</a>
                    </li>
					<li class="nav-item">
                        <a class="nav-link" href="#" id="menu-projects">Projects</a>
                    </li>
				</ul>
                <ul class="navbar-nav ms-3">
					<li class="nav-item">
                        <a class="nav-link" href="#" id="menu-contact">CONTACT</a>
                    </li>
                </ul>
			</div>
		</nav>
	</div>
    </div>
</template>
<script>
export default {
    name: "Navbar",
};
</script>
<style scoped>
    button{
        outline: none;
        border: none;
        box-shadow: none;
    }
    button:focus{
        outline: none;
        border: none;
        box-shadow: none;
    }
    svg{
        color: white;
    }
    #navbar-container{
        background-color: #3DBEFF;
    }
    #navbar-name{
        color: white;
        letter-spacing: 1px;
        font-family: 'Barlow', sans-serif;
        font-weight: 800;
        padding-left: 1em;
    }
    #menu-about,#menu-services,#menu-projects{
        color: white;
        font-weight: 400;
    }
    #menu-contact{
        font-weight: 800;
        font-size: 13px;
        background-color: white;
        border-radius: 50px;
        padding: 10px 19px;
    }
    #menu-contact:hover{
        background-color: #6fcfff;
        color: white;
    }
    #MenuNavegacion{
        padding: 0 1em;
    }

    .about,.services,.projects,.contact{
        color: black;
        font-family: 'Barlow', sans-serif;
        font-weight: 700;
        text-align: center;
    }
    .contact{
        background-color: #fed000;
        border-radius: 50px;
        padding: 10px 19px;
    }
</style>