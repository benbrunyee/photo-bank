<div
  class="gradient absolute left-0 top-0 flex h-full w-full items-center justify-center rounded-md {$$props.class}"
  style={$$props.style ?? ""}
/>

<style>
  .gradient {
    background: linear-gradient(
      90deg,
      rgba(215, 215, 215, 1),
      rgba(245, 245, 245, 1),
      rgba(215, 215, 215, 1)
    );
    background-size: 400% 400%;
    animation: gradient-fade 1.5s ease-in-out infinite;
  }

  @keyframes gradient-fade {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }
</style>
