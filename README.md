[Question on Stack Overflow][1]

--------------------------------------

I'm trying to inject some images into my pages created from markdown. I'm trying to do this using ReactDomServer.renderToString()

    const componentCreatedFromMarkdown = ({data}) => {
    ...    
        useEffect(() => {
            const injectDivs = Array.from(document.getElementsByClassName('injectDivs'))
            injectDivs.forEach((aDiv) => {
                aDiv.innerHTML = ReactDOMServer.renderToString(<Img fluid={data.allFile.edges[0].node.childImageSharp.fluid} />)
            }
        })
    ...
    }


The img is showing as a black box, if I right click the image I can open it in a new tab, which shows the image as it is supposed to be.

---------------------------------------

[![enter image description here][2]][2]


  [1]: https://stackoverflow.com/questions/62688539/injecting-gatsby-image-into-html-which-was-created-from-markdown-using-reactdo
  [2]: https://i.stack.imgur.com/BPkSO.png
