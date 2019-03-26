---
title: Testing
content:
  - javascript: |-
      var input = {
          "image": "data://deeplearning/example_data/lincoln.jpg"
      };
      Algorithmia.client("simqDc5VqlkqkM3CvwDeo4KuMZ/1")
          .algo("deeplearning/ColorfulImageColorization/1.1.13?timeout=300") // timeout is optional
          .pipe(input)
          .then(function(output) {
              console.log(output);
          });
    python: |-
      import Algorithmia

      input = {
        "image": "data://deeplearning/example_data/lincoln.jpg"
      }
      client = Algorithmia.client('simqDc5VqlkqkM3CvwDeo4KuMZ/1')
      algo = client.algo('deeplearning/ColorfulImageColorization/1.1.13')
      algo.set_options(timeout=300) # optional
      print(algo.pipe(input).result)
    r: |-
      library(algorithmia)

      input <- list("image"="data://deeplearning/example_data/lincoln.jpg")
      client <- getAlgorithmiaClient("simqDc5VqlkqkM3CvwDeo4KuMZ/1")
      algo <- client$algo("deeplearning/ColorfulImageColorization/1.1.13")
      algo$setOptions(timeout=300) # optional
      result <- algo$pipe(input)$result
      print(result)
    scala: >-
      import com.algorithmia._

      import com.algorithmia.algo._


      val input = """{
        "image": "data://deeplearning/example_data/lincoln.jpg"
      }"""

      val client = Algorithmia.client("simqDc5VqlkqkM3CvwDeo4KuMZ/1")

      val algo =
      client.algo("deeplearning/ColorfulImageColorization/1.1.13?timeout=300")
      // timeout is optional

      val result = algo.pipeJson(input)

      System.out.println(result.asString)
    type: code-sample
---

