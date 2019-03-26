---
title: Getting Started
content:
  - content: This is some markdown content...
    type: markdown
  - javascript: >-
      var input =
      {"image":"data://pmcq/asdf/colorful_image_colorization_description_image.png"};

      Algorithmia.client("simLaRB/JSnIjO9k80a2IZ+v4DI1",
      "https://api.test.algorithmia.com")
          .algo("algorithmiahq/ColorfulImageColorization/0.1.4?timeout=300") // timeout is optional
          .pipe(input)
          .then(function(output) {
              console.log(output);
          });
    python: >-
      import Algorithmia


      input = {
        "image": "data://pmcq/asdf/colorful_image_colorization_description_image.png"
      }

      client = Algorithmia.client('simLaRB/JSnIjO9k80a2IZ+v4DI1',
      'https://api.test.algorithmia.com')

      algo = client.algo('algorithmiahq/ColorfulImageColorization/0.1.4')

      algo.set_options(timeout=300) # optional

      print(algo.pipe(input).result)
    r: >-
      library(algorithmia)


      input <-
      list("image"="data://pmcq/asdf/colorful_image_colorization_description_image.png")

      client <- getAlgorithmiaClient("simLaRB/JSnIjO9k80a2IZ+v4DI1",
      "https://api.test.algorithmia.com")

      algo <- client$algo("algorithmiahq/ColorfulImageColorization/0.1.4")

      algo$setOptions(timeout=300) # optional

      result <- algo$pipe(input)$result

      print(result)
    scala: >-
      import com.algorithmia._

      import com.algorithmia.algo._


      val input = """{
        "image": "data://pmcq/asdf/colorful_image_colorization_description_image.png"
      }"""

      val client = Algorithmia.client("simLaRB/JSnIjO9k80a2IZ+v4DI1",
      "https://api.test.algorithmia.com")

      val algo =
      client.algo("algorithmiahq/ColorfulImageColorization/0.1.4?timeout=300")
      // timeout is optional

      val result = algo.pipeJson(input)

      System.out.println(result.asString)
    type: code-sample
---

