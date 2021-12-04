<script lang="ts">
  import logo from "./assets/svelte.png";
  import Counter from "./lib/Counter.svelte";
  import SimpleComponent from "./lib/SimpleComponent.svelte";
  import DirectiveHtml from "./lib/DirectiveHtml.svelte";
  import ReactiveDeclaration from "./lib/ReactiveDeclaration.svelte";
  import Nested from "./lib/Nested.svelte";
  import SpreadProps from "./lib/SpreadProps.svelte";
  import IfLogic from "./lib/IfLogic.svelte";
  import LoopLogic from "./lib/LoopLogic.svelte";
  import DomEvent from "./lib/event/DomEvent.svelte";
  import EventModifier from "./lib/event/EventModifier.svelte";
  import Event from "./lib/event/Event.svelte";
  import Binding from "./lib/binding/Binding.svelte";
  import LifeCycle from "./lib/lifecycle/LifeCycle.svelte";
  import Store from "./lib/store/Store.svelte";
  import SlotDefault from "./lib/slot/SlotDefault.svelte";

  const spreadPropsValue = {
    name: "dd",
    version: 1,
    speed: 1231,
    href: "www.naver.com",
  };
</script>

<main>
  <!-- <DirectiveHtml />
  <SimpleComponent />
  <ReactiveDeclaration />
  <Nested answer={"42"} />
  <SpreadProps {...spreadPropsValue} />
  <IfLogic />
  <Counter />
  <LoopLogic />
  <DomEvent /> 
  <Event />
  <Binding />
  <LifeCycle />-->

  <Store />
  <SlotDefault />
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
