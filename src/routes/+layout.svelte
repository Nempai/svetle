<nav>
    <div class="nav-container">
      <a href="/" class="nav-logo" title="Back to Homepage">Данил Самсонов</a>
      <div class="nav-links">
        {#each nav as link}
        <a href={link.href} class="link">{link.title}</a>
        {/each}
      </div>
    </div>
  </nav>
  <div class="container">
    <slot />
  </div>

    <style>
            .container {
      max-width: 1400px;
      margin: 50px auto;
    }
			body {
			  background-position: left top;
			  font-family: "Inter", sans-serif;
			  margin: 0;
			  background-repeat: no-repeat;
			}
	  
			* {
			  box-sizing: border-box;
			}
	  
			a {
			  text-decoration: none;
			  color: black;
			}
	  
			nav {
			  position: sticky;
			  top: 0;
			  left: 0;
			  right: 0;
			  margin: 0 80px 0 80px;
			  padding-top: 2rem;
			  padding-bottom: 2rem;
			}
	  
			nav .nav-container {
			  display: flex;
			  justify-content: space-between;
			  align-items: center;
			}
	  
			.nav-links {
			  display: flex;
			  justify-content: flex-end;
			  align-items: center;
			  margin: -1em 0;
			  flex: 1 0 auto;
			}
	  
			.nav-links .link {
			  position: relative;
			  margin: 1em;
			  font-size: 0.85rem;
			  letter-spacing: 1px;
			  color: black;
			}
	  
			.nav-logo {
			  position: relative;
			  line-height: 1;
			  font-size: 1.1rem;
			  color: black;
			}
		  </style>

    
    <script>
    const nav = [
    {
      title: 'Обо мне',
      href: '/about',
      isShow:true,
    },
    {
      title: 'Блог',
      href: '/blog',
      isShow:true,
    },
    {
      title: 'Портфолио',
      href: '/project',
      isShow:true,
    },
    {
      title: 'Контакты',
      href: '/contact',
      isShow:true,
    }
  ]
</script>


