You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "KGSK Alliance | About us",
      "first_heading": "ABOUT KGSK ALLIANCE"
    }
  },
  {
    "path": "blog.html",
    "context": {
      "title": "KGSK | Blogs",
      "first_heading": "BLOG"
    }
  },
  {
    "path": "blog_-kgsk-alliance-pvt-ltd--redefining-trust-and-integrity-in-international-trade-.html",
    "context": {
      "title": "\"KGSK Alliance Pvt Ltd: Redefining Trust and Integrity in International Trade\"",
      "first_heading": "\"KGSK Alliance Pvt Ltd: Redefining Trust and Integrity in International Trade\""
    }
  },
  {
    "path": "blog_-raisins--a-sweet-deal-for-b2b-buyers-exploring-opportunities-in-the-market.html",
    "context": {
      "title": "\u201cRaisins\u201d A Sweet Deal for B2B Buyers Exploring Opportunities in the Market",
      "first_heading": "\u201cRaisins\u201d A Sweet Deal for B2B Buyers Exploring Opportunities in the Market"
    }
  },
  {
    "path": "blog_-the-exquisite-flavour-journey-of-basmati-rice--exploring-varieties-and-culinary-delights-.html",
    "context": {
      "title": "\"The Exquisite Flavour Journey of Basmati Rice: Exploring Varieties and Culinary Delights\"",
      "first_heading": "\"The Exquisite Flavour Journey of Basmati Rice: Exploring Varieties and Culinary Delights\""
    }
  },
  {
    "path": "blog_by-products-of-raw-cashew-nuts.html",
    "context": {
      "title": "By-Products of Raw Cashew Nuts",
      "first_heading": "By-Products of Raw Cashew Nuts"
    }
  },
  {
    "path": "blog_cardamom-the-queen-of-spices---why-so-precious-for-us-.html",
    "context": {
      "title": "Cardamom-The Queen of Spices. Why so precious for us?",
      "first_heading": "Cardamom-The Queen of Spices. Why so precious for us?"
    }
  },
  {
    "path": "blog_green-moong-dal--a-tiny-bean-with-gigantic-potential.html",
    "context": {
      "title": "Green Moong Dal: A Tiny Bean with Gigantic Potential",
      "first_heading": "Green Moong Dal: A Tiny Bean with Gigantic Potential"
    }
  },
  {
    "path": "blog_impact-of-covid-19-on-businesses-.html",
    "context": {
      "title": "Impact Of Covid-19 On Businesses",
      "first_heading": "Impact Of Covid-19 On Businesses"
    }
  },
  {
    "path": "blog_makhana---tap-the-untapped-market.html",
    "context": {
      "title": "Makhana - Tap the Untapped Market",
      "first_heading": "Makhana - Tap the Untapped Market"
    }
  },
  {
    "path": "blog_new-opportunities---how-covid-19-has-brought-success-to-export-business-.html",
    "context": {
      "title": "New Opportunities! How Covid\u201919 has brought success to Export Business!",
      "first_heading": "New Opportunities! How Covid\u201919 has brought success to Export Business!"
    }
  },
  {
    "path": "blog_seizing-opportunities-in-the-organic-chickpea-boom.html",
    "context": {
      "title": "Seizing Opportunities in the Organic Chickpea Boom",
      "first_heading": "Seizing Opportunities in the Organic Chickpea Boom"
    }
  },
  {
    "path": "blog_tunisian-treasures--sweetening-your-success-with-kgsk-alliance.html",
    "context": {
      "title": "Tunisian Treasures: Sweetening Your Success with KGSK Alliance",
      "first_heading": "Tunisian Treasures: Sweetening Your Success with KGSK Alliance"
    }
  },
  {
    "path": "blog_types-of-rice-grains.html",
    "context": {
      "title": "Types Of Rice Grains",
      "first_heading": "Types Of Rice Grains"
    }
  },
  {
    "path": "career.html",
    "context": {
      "title": "KGSK | Career",
      "first_heading": "CAREEREmail: careers@kgskalliance.com"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "KGSK | Contact Us",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/0e222dfb63e9e8efe16d4082244ac3e1.css",
    "context": {
      "path": "css/0e222dfb63e9e8efe16d4082244ac3e1.css"
    }
  },
  {
    "path": "css/49c841b73a78e7c317e7d11ae22224b7.css",
    "context": {
      "path": "css/49c841b73a78e7c317e7d11ae22224b7.css"
    }
  },
  {
    "path": "css/4a0f72ccd0263ec1d22c2d3d39184b8a.css",
    "context": {
      "path": "css/4a0f72ccd0263ec1d22c2d3d39184b8a.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/87b794ec556b63cc51afb001d70fc32a.css",
    "context": {
      "path": "css/87b794ec556b63cc51afb001d70fc32a.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/b6bca29a045ccea29d3ad6f0a396bc42.css",
    "context": {
      "path": "css/b6bca29a045ccea29d3ad6f0a396bc42.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/ee28a3d5945c8844a3dd66afa1428995.css",
    "context": {
      "path": "css/ee28a3d5945c8844a3dd66afa1428995.css"
    }
  },
  {
    "path": "css/fb4315453525b92819aa8f2133f47c2a.css",
    "context": {
      "path": "css/fb4315453525b92819aa8f2133f47c2a.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "export-products.html",
    "context": {
      "title": "KGSK Alliance | Export Products",
      "first_heading": "EXPORT PRODUCTSRice| Processed Cashew Nuts | Spices | Pulses | Raisins"
    }
  },
  {
    "path": "imgs/03601d53bf025c296c7736cb025db340.webp",
    "context": {
      "refs": [
        {
          "alt": "Liberia",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/05b5d2730007b81a18c7e4dd83e6d648.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/07835ad728a3617edca112c28d7e5da7.webp",
    "context": {
      "refs": [
        {
          "alt": "Pulses",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0947b39e761b6904d06f69e0215391c1.webp",
    "context": {
      "refs": [
        {
          "alt": "1121 Steam Extra Long Grain Rice",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0a78e3eddfea6f34d45d673a4bcace0d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c92f4d48124944633ac86a1b80ddbf8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/187238c9fbdddf2bc84aa5169d22c42f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1a03a8aff61cabf45e093c119e70a08d.webp",
    "context": {
      "refs": [
        {
          "alt": "Benin",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b28d22b1acabf4df436ba784b57f676.webp",
    "context": {
      "refs": [
        {
          "alt": "Senegal",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/201c33f05cbfb771693e39a9469bb468.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2340fdf881efc9450e046f3990c2167d.webp",
    "context": {
      "refs": [
        {
          "alt": "1.Importer and Exporter of Agro Products India 2.Raw Cashew Nuts Importer and Supplier India 3.Proce",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25e078949347aaf5f1761f22f871f09f.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/26795446757ac199a6c81d83ab831561.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/293d61bc709cba7790b15de19634b441.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2bf048d312040c2dcf9415258698b353.webp",
    "context": {
      "refs": [
        {
          "alt": "Sierra Leone",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c696a0c3cf8fd52fd99f9466df77218.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e53ac253437c0323a3a12a7a4b8bd69.webp",
    "context": {
      "refs": [
        {
          "alt": "Exports",
          "title": ""
        },
        {
          "alt": "Imports",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2f0f503492161d3158892346ccf3e039.webp",
    "context": {
      "refs": [
        {
          "alt": "ADEPACertificate",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/372c0b1e827f7cf0fc88baed3a24834e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/40f16bd5eb4682cb6012aa695e07a26e.webp",
    "context": {
      "refs": [
        {
          "alt": "India",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/42f4f5d577a4293c719ba0d00526dc6f.webp",
    "context": {
      "refs": [
        {
          "alt": "Dry Red Chilly",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4342e27a00683238ad6f66bb3d78f196.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46645f229e5f731da3b7af7e276161e0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4754b80ed44ba03339f75e045db40614.webp",
    "context": {
      "refs": [
        {
          "alt": "Turmeric",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4bf27ff995f41c5643b371fdc6737ad0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4cd6e2712615b1a403830333d6fd5848.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4fefaa4f338cf60e6b4bf88de0c84a80.webp",
    "context": {
      "refs": [
        {
          "alt": "IR 64 Paraboiled",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5109fc21e3715967e08f239000321674.webp",
    "context": {
      "refs": [
        {
          "alt": "ADEPACertificate",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/51fa4b4cd167d4d275b840bd6534b66a.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5235b9e79d8a5b60881afe92f205068b.webp",
    "context": {
      "refs": [
        {
          "alt": "We are one of the fastest growing international trading companies.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/52f161ad0179865fba3723cdf074d281.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55377f2fc83236e9f14ebfd16492ec28.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55f32353dd464c7572696e48f5b46591.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5829424c562de8617282c43de3214396.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e7b53d3a1dd28b13d868a19c18140cd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62734b1cb16445b711382b1e5f896456.webp",
    "context": {
      "refs": [
        {
          "alt": "Nigeria",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62d6f3571a792d297f241cd1091e5fe4.webp",
    "context": {
      "refs": [
        {
          "alt": "Certified and Authentic",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6452564a0fe025d7f4f450cb3a66f6f7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64ff0d8aa3a1ce01a86f20fd64b64a93.webp",
    "context": {
      "refs": [
        {
          "alt": "Long Standing Experience",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/663f83a4ce496675e22ab330940fdde2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67db1d0f44e009e8e7b5acc177088c2a.webp",
    "context": {
      "refs": [
        {
          "alt": "COI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6ce8d61b7c6685cdec2d282c7a2ca525.webp",
    "context": {
      "refs": [
        {
          "alt": "COI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d2ef2b34b6a94f28f6a35cf949ae04e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6eeaeb8b3da0903e4980f65b71f691b1.webp",
    "context": {
      "refs": [
        {
          "alt": "Indonesia",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6f4ce7bbe4f4482e34b0ccaaeee558ca.webp",
    "context": {
      "refs": [
        {
          "alt": "IR 64 (Raw/White)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/719bf1327f0dbe5e9e7c8f9af0e6ae1b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7606e813c660987ed74a92e7f5d400b2.webp",
    "context": {
      "refs": [
        {
          "alt": "Pusa Steam Basmati Rice",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/77c38981ae87da080a86a963f2e7d131.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78adfce40142f2eb77b8e8423fa85902.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/790a7aea1d00499f7a212e122b54c65c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f72ee2d029624931209078b0be2c710.webp",
    "context": {
      "refs": [
        {
          "alt": "ADEPACertificate",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/813fed5c5c4bdedb050e7bf9c53181ea.webp",
    "context": {
      "refs": [
        {
          "alt": "cote di voire",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81473c13495671830296e23d33370620.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8938731627da6cbcd71c159e7d944ab2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f8fbe65c95b71e45d50388991ea1002.webp",
    "context": {
      "refs": [
        {
          "alt": "KGSK Alliance is one of the most trusted and fastest growing exporters of rice, onions, finished cas",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/972ef2a419aa2f982bc6785e81405d49.webp",
    "context": {
      "refs": [
        {
          "alt": "Sesame Seeds",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9bfeac943140b8b39a5d8d5af0ed8e03.webp",
    "context": {
      "refs": [
        {
          "alt": "Sona Masoori",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9cfc43c53d9847ab551c5c1eef97c109.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ddb1a156f80a1a86550c3318e2a1df7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e7fbab91b3c301bc57438bc6990cc26.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/a0571027350c3d0e7c674e4a9d47852b.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a1e752b905e0ea866217a2e7b8b1f271.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a2d86476cb5407c1d464427503fda0eb.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a6f25a5e2bb424dd8161e5f0220035c1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aa69a1a37fd3b93dfadc9112a7341ed8.webp",
    "context": {
      "refs": [
        {
          "alt": "KGSK Alliance Pvt Ltd, ethical business practices, international trade, customer satisfaction, impor",
          "title": ""
        },
        {
          "alt": "raisin market, B2B trade, raisin supplier, KGSK Alliance, dried grapes, nutrient-packed, antioxidant",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad61e1c05997b1714d5b83fac0e38ed3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b08679ab23a78a6a0787e8a23c30767a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2340580fcd73e5b004d4ef21089da01.webp",
    "context": {
      "refs": [
        {
          "alt": "Togo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2a055b6a3c7c8a19dab6d2ba2859356.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2d8c80e1e351dac5a181b3353055701.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4dc4d612e4500350276b7bd94f10cb9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b71ff5c17a945f1a6b61a09db7efc90a.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b816efc1eac7d6dc3f4770121b50b517.webp",
    "context": {
      "refs": [
        {
          "alt": "1121 Sella Basmati Rice",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8e1b56a7f18b964c345f9d6b5fd2c15.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Vision",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf61c32cf779dfb423f68ed919e213ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c2a3e32b2fe15d9ec6e3f8a67ccb025f.webp",
    "context": {
      "refs": [
        {
          "alt": "COI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6fc93a8ffb58f0b6e24ee3aaa65c1f7.webp",
    "context": {
      "refs": [
        {
          "alt": "High-Quality Service",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c847f5abe10b48a373390895b3f49b2c.webp",
    "context": {
      "refs": [
        {
          "alt": "Raw Cashew Nuts",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c8dd5cab38929fbcc97d25ca489c969b.webp",
    "context": {
      "refs": [
        {
          "alt": "Rice",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cba1be27f19e05df340dba04c29e9dc2.webp",
    "context": {
      "refs": [
        {
          "alt": "Soybean Seeds",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cc24519b2e61e3413426249ff7a1e872.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ccd0a8076cc1994b56a2c5784850fac2.webp",
    "context": {
      "refs": [
        {
          "alt": "Cumin Seeds",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd612d1034e01b86220fe1278a885577.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cdd4f80d7f4912fac6aa59e172fb4a83.webp",
    "context": {
      "refs": [
        {
          "alt": "Creativity Meets Excellence",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfd40956beb87c1636ffdde437f641d8.webp",
    "context": {
      "refs": [
        {
          "alt": "Ghana",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d12cf57df6dbd00bc20ebcc8cb38ddb3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d13c7ac43733a700dc3c8c621232fd0a.webp",
    "context": {
      "refs": [
        {
          "alt": "Finished Cashew Nuts",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d83dbf5b5722385e118fe04bae096272.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Mission",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d89d3772f6af14b01518f664275580dd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dcd3b993c2691abcf014b5a9d578743d.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e08e417c4716b9c13dd8fc3f9394f621.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e3ec59847597c40b709cf74ac4f28f9f.webp",
    "context": {
      "refs": [
        {
          "alt": "1121 Golden Sella Basmati Rice",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e45f413b5e5a73d3ac43aa1c2ffd2eb5.webp",
    "context": {
      "refs": [
        {
          "alt": "Chile Walnut",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e483e1ddc9d2409417280a6cf29ba6a6.webp",
    "context": {
      "refs": [
        {
          "alt": "Raw Cashew Nuts",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e4e12be9f6b0f2868cde7ba54912e3ab.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e6ae74dc7f54285ed4a92b7d8e73c2c6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e7fe290220b61273f6833d5f030fe3f9.webp",
    "context": {
      "refs": [
        {
          "alt": "Australia",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e922f427cc9c3d00aa07202f0b12bd37.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ea22539663554772956e7e089c9424ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ea9353622f788370f6b6a9dedeba2dd0.webp",
    "context": {
      "refs": [
        {
          "alt": "Pistachio",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec8d718f0921d0e97bcb0bc999965390.webp",
    "context": {
      "refs": [
        {
          "alt": "New Zealand",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef66881ae12897f88cbb39fa064f3ed1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f074954a66c8b3cd60fb82c0d858ae04.webp",
    "context": {
      "refs": [
        {
          "alt": "We Value Time With 100% Commitment",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0a4c3b686e90a24b84772484ccf7695.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f68fcfc1c0290a15690a809bd8025528.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f69f5b178a61e1753189394cfe7dbb53.webp",
    "context": {
      "refs": [
        {
          "alt": "Pulses",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f8dda16da7f96d5a515aa797929357b6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fcca6bb61c9c8c41491a3b9c87f809bb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "import-products.html",
    "context": {
      "title": "KGSK Alliance | Import Products",
      "first_heading": "IMPORT PRODUCTSRaw Cashew Nuts | Soyabean | Dates | Dry Spilt Ginger"
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "KGSK Alliance | Home",
      "first_heading": "KGSK ALLIANCE"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/4ac39d287f795add9fb2b7727b39f406.js",
    "context": {
      "path": "js/4ac39d287f795add9fb2b7727b39f406.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "rice.html",
    "context": {
      "title": "KGSK Alliance | Rice",
      "first_heading": "RICERanging from Basmati to Non-Basmati varieties of rice"
    }
  },
  {
    "path": "services.html",
    "context": {
      "title": "KGSK | Services",
      "first_heading": "International Trade"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.