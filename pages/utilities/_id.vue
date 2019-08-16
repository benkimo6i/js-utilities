<template>
  <div class="container">
    <div class="utility-content">
      <h1 class="utility-title title">{{ post.title }}</h1>
      <p class="utility-author subtitle"><span>By</span> <a :href="post.github">{{post.author}}</a></p>
      <p class="utility-desc">{{ post.description }}</p>
      <div class="utility-code">
        <pre class="prettyprint">
          <code class="prettyprint">{{ post.code }}</code>
        </pre>
      </div>
    </div> 
    <n-link class="site-link" to="/">Back</n-link>
  </div>
</template>

<script>
  export default {
    head () {
      return {
        script: [
          { src: 'https://cdn.jsdelivr.net/gh/google/code-prettify@master/loader/run_prettify.js' }
        ]
      }
    },
    data () {
      return {
        id : this.$route.params.id,
        utilities: [
          {
            author: 'John Moore',
            code: "\r\n \/**\r\n * This is a function to get cookies.\r\n *\r\n * @param {string} name - A string param\r\n * @return {string} A good string\r\n *\r\n * @example\r\n *\r\n * getCookie('viewed')\r\n *\/\r\n\r\nexport function getCookie(name) {\r\n  const cookies = {}\r\n  const cookieSet = document.cookie.split('; ');\r\n  cookieSet.forEach(cookie => cookies[cookie.split('=')[0]] = cookie.split('=')[1]);\r\n\r\n  return cookies[name];\r\n};",
            description: 'Utility function for getting browser cookies',
            github: 'https://github.com/ghlost',
            id: 'get-cookies',
            title: 'Get Cookies'
          }
        ]
      }
    },
    computed: {
      post () {
        return this.utilities.find(utility => utility.id === this.id);
      }
    }
  }
</script>

<style>
/* Pretty printing styles. Used with prettify.js. */
/* Vim sunburst theme by David Leibovic */

pre .str, code .str { color: #65B042; } /* string  - green */
pre .kwd, code .kwd { color: #E28964; } /* keyword - dark pink */
pre .com, code .com { color: #AEAEAE; font-style: italic; } /* comment - gray */
pre .typ, code .typ { color: #89bdff; } /* type - light blue */
pre .lit, code .lit { color: #3387CC; } /* literal - blue */
pre .pun, code .pun { color: #fff; } /* punctuation - white */
pre .pln, code .pln { color: #fff; } /* plaintext - white */
pre .tag, code .tag { color: #89bdff; } /* html/xml tag    - light blue */
pre .atn, code .atn { color: #bdb76b; } /* html/xml attribute name  - khaki */
pre .atv, code .atv { color: #65B042; } /* html/xml attribute value - green */
pre .dec, code .dec { color: #3387CC; } /* decimal - blue */

pre.prettyprint, code.prettyprint {
	background-color: #000;
  border: 0 !important;
	border-radius: 4px;
}

pre.prettyprint {
	width: 95%;
	margin: 1em 0;
	padding: 30px !important;
	white-space: pre-wrap;
}


/* Specify class=linenums on a pre to get line numbering */
ol.linenums { margin-top: 0; margin-bottom: 0; color: #AEAEAE; } /* IE indents via margin-left */
li.L0,li.L1,li.L2,li.L3,li.L5,li.L6,li.L7,li.L8 { list-style-type: none }
/* Alternate shading for lines */
li.L1,li.L3,li.L5,li.L7,li.L9 { }

@media print {
  pre .str, code .str { color: #060; }
  pre .kwd, code .kwd { color: #006; font-weight: bold; }
  pre .com, code .com { color: #600; font-style: italic; }
  pre .typ, code .typ { color: #404; font-weight: bold; }
  pre .lit, code .lit { color: #044; }
  pre .pun, code .pun { color: #440; }
  pre .pln, code .pln { color: #000; }
  pre .tag, code .tag { color: #006; font-weight: bold; }
  pre .atn, code .atn { color: #404; }
  pre .atv, code .atv { color: #060; }
}
</style>