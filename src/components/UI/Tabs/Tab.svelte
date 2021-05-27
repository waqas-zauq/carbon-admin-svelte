<script>
  export let id;
  const handleClick = e => {
    e.preventDefault();
    const target = e.target;
    let headParent = target.parentElement.parentElement;
    let contentParent = headParent.nextElementSibling;
    headParent.querySelectorAll("li").forEach(el => {
      let element = el.firstChild;
      element.classList.remove("active");
    });
    contentParent.querySelectorAll(".tab-pane").forEach(nel => {
      if (nel.id === `${id}`) {
        nel.classList.add("show", "active");
      } else {
        nel.classList.remove("show", "active");
      }
    });
    if (target.id === `${id}-tab`) {
      target.classList.add("active");
    }
  };
</script>

<li class="nav-item" role="presentation">
  <a
    class={`nav-link`}
    id={`${id}-tab`}
    data-toggle="tab"
    href={`#${id}`}
    role="tab"
    aria-controls={id}
    on:click={handleClick}>
    <slot />
  </a>
</li>
