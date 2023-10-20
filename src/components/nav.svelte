<script>
    let isOpen = false;
  
    function toggleMenu() {
      isOpen = !isOpen;
    }
  </script>
  
  <div class="sticky-menu">
    <div class="menu-icon {isOpen ? 'active' : ''}" on:click={toggleMenu}>
      {"<3"}
    </div>
    <div class="menu-items {isOpen ? 'active' : ''}">
        <a href="#" class="menu-item" on:click={toggleMenu}>Home</a>
        <a href="#" class="menu-item" on:click={toggleMenu}>About Me</a>
        <a href="#" class="menu-item" on:click={toggleMenu}>Work</a>
        <a href="#" class="menu-item" on:click={toggleMenu}>Contact</a>
    </div>
  </div>
  
  <style>
    .sticky-menu {
      position: fixed;
      top: 0;
      right: 0;
      background-color: #251b31c9;
      width: 4rem;
      height: 4rem;
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }
  
    .menu-icon {
      color: #fff;
      font-size: 24px;
      cursor: pointer;
      user-select: none;
      transition: transform 0.2s ease, color 0.1s;
    }
  
    .menu-icon:active {
      transform: scale(0.9);
      color: #df5757;
    }
  
    @media (max-width: 768px) {
      .menu-icon,
      .menu-item {
        transition: transform 0.2s ease, color 0.1s;
      }
  
      .menu-icon:active,
      .menu-item:active {
        color: #df5757; 
        transform: scale(0.9); 
      }
    }
  
    .menu-items {
      position: absolute;
      top: 4rem;
      right: 0;
      background-color: #251b31c9;
      width: 200px;
      padding: 10px;
      display: none;
      flex-direction: column;
      align-items: right;
    }
  
    .menu-items.active {
      display: flex;
      flex-direction: column;
      justify-content: right;
      align-items: right;
      animation: fadeIn 0.5s ease;
    }
  
    @keyframes fadeIn {
      from {
        opacity: 0;
      }
      to {
        opacity: 1;
      }
    }
  
    .menu-item {
      margin: 10px;
      font-size: 18px;
      cursor: pointer;
      color: white;
      user-select: none;
      text-decoration: none;
      font-size: 1.5rem;
    }
  
    .menu-item:active {
      transform: scale(0.9);
      transition: transform 0.2s ease;
      user-select: none;
      text-decoration: none;
    }
  
    .menu-item:hover {
      color: #df5757;
    }
  </style>
  