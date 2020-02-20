<script>
export default {
  functional: true,
  props: {
    isNext: {
      default: true
    }
  },
  render(h, context) {
    var data = {
      props: {
        appear: true,
        appearActiveClass: "animated fadeIn",
        enterActiveClass: context.props.isNext ? "animated fadeIn" : "animated fadeIn",
        leaveActiveClass: context.props.isNext ? "animated fadeOut" : "animated fadeOut",
        name: "data-driven-transition",
        duration: 1000,
        mode: "out-in"
      }
    }
    return h("transition-group", data, context.children)
  }
}
</script>
