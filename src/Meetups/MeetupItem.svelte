<script>
  import Button from "../UI/Button.svelte";
  export let title;
  export let subtitle;
  export let imgURL;
  export let description;
  export let email;
  export let address;
</script>

<style>
    article {
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
      border-radius: 5px;
      background: white;
      margin: 1rem;
    }
  
    header,
    .content,
    footer {
      padding: 1rem;
    }

    .content {
      height: 4rem;
    }
  
    .image {
      width: 100%;
      height: 14rem;
    }
  
    .image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  
    h1 {
      font-size: 1.25rem;
      margin: 0.5rem 0;
      font-family: "Roboto Slab", sans-serif;
    }
  
    h1.is-favorite {
      background: #01a129;
      color: white;
      padding: 0 0.5rem;
      border-radius: 5px;
    }
  
    h2 {
      font-size: 1rem;
      color: #808080;
      margin: 0.5rem 0;
    }
  
    p {
      font-size: 1.25rem;
      margin: 0;
    }
  
    div {
      text-align: right;
    }
  </style>
  
  <article>
    <header>
      <h1>{title}</h1>
      <h2>{subtitle}</h2>
      <p>{address}</p>
    </header>
    <div class="image">
      <img src="{imgURL}" alt="{title}" />
    </div>
    <div class="content">
      <p>{description}</p>
    </div>
    <footer>
      <Button href="mailto:{email}" caption={email} />
      <Button type="button" mode="outline" caption="Favourite" />
      <Button type="button" caption="Show Details" />
    </footer>
  </article>
  