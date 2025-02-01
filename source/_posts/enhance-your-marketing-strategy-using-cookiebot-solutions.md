---
title: Enhance Your Marketing Strategy Using Cookiebot Solutions
date: 2025-01-24T23:08:23.344Z
updated: 2025-01-31T21:28:47.707Z
categories:
  - abbyy
thumbnail: https://thmb.techidaily.com/a65a2d3fb958e05df694286812a1e2454a9d6c6ff463421241eb49561be7ce4c.jpg
---

## Enhance Your Marketing Strategy Using Cookiebot Solutions

[Back to The Intelligent Enterprise](https://tools.techidaily.com/abbyy/products/)

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/it8VkxDUdAc?si=ef6VZWR7kW4P9ikh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## Pushing the Boundaries of IDP: Object Detection, Word Recognition, and Key-Value Extraction

###### by Max Vermeir, Senior Director of AI Strategy

One of the most defining characteristics of IDP is the strategic use of AI as the core foundation for automating document-centric tasks. ABBYY developers explain three exciting new AI models that are pushing the boundaries of IDP in key-value extraction, object detection, and word recognition.

One of the most defining characteristics of intelligent document processing (IDP) is the strategic use of artificial intelligence (AI) as the core foundation for automating document-centric tasks. AI models and algorithms enable contextual understanding to improve speed and accuracy, driving business value for customers with document-heavy workflows. 

[ABBYY Vantage](https://tools.techidaily.com/abbyy/products/) exemplifies this concept with its library of pre-trained “skills,” also known as pre-trained AI document processing models. By narrowing the scope of an AI solution to excel at a specific task, these purpose-built AI skills work efficiently to accelerate outcomes in specialized contexts. 

In a recent showcase session presented by the ABBYY research and development team, our developers Konstantin Anisimovich, Evgenii Orlov, Ivan Zagaynov, and Andrew Upshinskiy explained three exciting new AI models that are pushing the boundaries of IDP in key-value extraction, object detection, and word recognition.

#### 1\. Key-value extraction 

Identifying key information is an essential Vantage skill that allows for actionable data to be extracted from a document type. Document-specific models at the core of the skill are trained to identify fields such as “company name,” “address,” or “zip code,” enabling the corresponding values to be extracted. Separate models are made for different document types, determining the fields that the model will look for.

This process is known as **key-value pairs extraction**. This entails finding all possible “keys,” or field names; all possible “values,” which are the contents of those fields; as well as the associations between keys and corresponding values. But how is the model trained to make these associations?

Taking a large, general key-value extraction model and training it on a set of documents allows the model to build proficiency in automatic markup. Through a process called **knowledge distillation**, or the transferring of knowledge from a large AI model to a smaller one, more specialized AI models can be built that operate at a lower computational cost and greater inference speeds, than their larger counterparts.

ABBYY’s current path towards this solution consists of two independent workflows: entity extraction and linking models for general documents, and key summarization and QA models for text-heavy documents such as contracts. Both models are based on the transformer architecture that is ubiquitous in modern neural networks, e.g., the GPT-family and other LLMs.

![pushing-the-boundaries-of-idp-2](https://content.abbyy.com/-/media/project/abbyy/abbyy/insights/intelligent-enterprise/content-media/pushing-the-boundaries-of-idp-2.png)

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/w7c5EHp-GDw?si=UTw7lZR0wTmRjp8W" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

The image above portrays a form-like document where green highlights indicate keys, and yellow highlights indicate values that must be extracted from their respective keys. In a form, there are visual indicators such as layouts and blank cells that suggest where key-values lie. The world classification model tags each word as either a background or a part of a key or value, while the entity linking model combines the tagged words into key/value sequences and matches them together. Within this workflow, text is processed by a RoBERTa transformer, while visual data (images) are processed by a compact YOLOv8 model.

For text-heavy documents, a text summarization model extracts a list of all keys from the document, and a question-answering model finds corresponding value excerpts using information about the key. Once again, two separate models are used in this workflow: for key extraction, an encoder-decoder architecture uses a multimodal LayoutLM-like transformer encoder to extract rich features from the data, and a BART transformer decoder extracts relevant key word sequences using the encoded data. The value extraction model is based on a RoBERTa transformer and employs query paraphrasing and adversarial data to enhance performance.

Webinar

#### The AI within Your IDP Platform

[Learn more](https://tools.techidaily.com/abbyy/products/)

#### 2\. Detecting objects in a document image

Object detection is a crucial stage of document processing, as elementary objects must eventually be extracted from the document. This entails estimating the size of the text, correcting the skew of a page, adjusting images to a normalized state, and other variables before objects can be extracted.

A document can be thought of as a “bag of objects,” with such objects including signatures, stamps, checkmarks, separators, barcodes, printed and handwritten text, and other possible entities.

Historically, there have been two approaches to this detection: classic methods and neural networks.

Classic methods are based on well-known and trusted algorithms but tend to be limited in their ability to handle photos and corrupted documents. This can introduce complications when dealing with shadows, distortion, and other forms of visual noise, impacting results in the object detection stage. Neural networks, by contrast, are a state-of-the-art solution that ABBYY has already used for over five years, yielding optimal results in detecting various kinds of objects. However, this requires a neural network for each object type, making this approach unfeasible when detecting multiple object varieties.

As such, ABBYY came to a solution involving a universal feature extractor common to several object detection nets within a neural network. This “backbone net” delegates feature extraction to several detection heads, each with a unique architecture allowing them to detect a specific object.

To consume less processing power in contexts requiring simultaneous data processing, this solution breaks document pages into several overlapping stripes, preserving objects that may occur at the boundary of each section. After processing each stripe, the contained objects are fed to detection heads and used for future tasks such as maintaining document structure or reconstructing paragraphs and tables. This process is called single-page parallel processing, as each striped section of a document can be processed by their respective detection heads in parallel.

#### 3\. Advanced word recognition

Traditional OCR involves an input of a line image containing text that then yields an output of a Unicode text sequence. The classic approach segments to approximate one-word fragments, finds the hypothesis for character segmentation points using a linear division graph, and finally constructs words from these hypotheses.

This approach can have complications. Segmentation points are often found heuristically; when the heuristic assumption is inadequate, the process will not work. In some languages, like Arabic and Bengali, there isn’t an easy heuristic case. This is also the case for handwritten text, which would require a level of script accuracy that is rare in handwriting.

As such, ABBYY developed an end-to-end approach for both handwritten and printed text recognition. An entire text sequence is extracted at once, removing the need for establishing boundaries within the document.

In printed cases, these documents are easy to identify elements and markup accordingly. This is an easier task for a neural network—the scan quality rate of the Latin model is 99.8 percent. The only flaw is inherent to the speed/quality balance. 

The architecture for end-to-end OCR generally consists of three parts: the backbone (visual transformer), which is responsible for image extraction; sequential modeling (transformer encoder), which is needed for some contextual features in an overall sequence; and the decoder, which is the algorithm determining how the text is ultimately written considering the feature set and previous steps in the process. This pipeline is then supplemented with ABBYY’s LLM that takes into account all the context of the recognition process and provides enhanced output of the recognized text, leading to incredible accuracy rates, especially in low-quality documents.

#### Evolving IDP: driving efficiency and versatility

The advances to ABBYY’s AI models reflect enterprises’ increasing need for agility and efficiency in document processing, not only in processing time, but also in energy consumption and general versatility. 

By broadening the capabilities of modern OCR with improved object detection, more inclusive word recognition, and the reliable extraction of actionable key values, ABBYY is expanding the scope of how intelligent document processing can transform business-critical processes.

Visit [abbyy.com/vantage](https://tools.techidaily.com/abbyy/products/) to learn more about purpose-built AI in IDP.

#### Subscribe for updates

Get updated on the latest insights and perspectives for business & technology leaders

First name\*

Last name

E-mail\*

Сountry\*

СountryAfghanistanAland IslandsAlbaniaAlgeriaAmerican SamoaAndorraAngolaAnguillaAntarcticaAntigua and BarbudaArgentinaArmeniaArubaAustraliaAustriaAzerbaijanBahamasBahrainBangladeshBarbadosBelgiumBelizeBeninBermudaBhutanBoliviaBonaire, Sint Eustatius and SabaBosnia and HerzegovinaBotswanaBouvet IslandBrazilBritish Indian Ocean TerritoryBritish Virgin IslandsBrunei DarussalamBulgariaBurkina FasoBurundiCambodiaCameroonCanadaCape VerdeCayman IslandsCentral African RepublicChadChileChinaChristmas IslandCocos (Keeling) IslandsColombiaComorosCongo (Brazzaville)Congo, (Kinshasa)Cook IslandsCosta RicaCroatiaCuraçaoCyprusCzech RepublicCôte d'IvoireDenmarkDjiboutiDominicaDominican RepublicEcuadorEgyptEl SalvadorEquatorial GuineaEritreaEstoniaEthiopiaFalkland Islands (Malvinas)Faroe IslandsFijiFinlandFranceFrench GuianaFrench PolynesiaFrench Southern TerritoriesGabonGambiaGeorgiaGermanyGhanaGibraltarGreeceGreenlandGrenadaGuadeloupeGuamGuatemalaGuernseyGuineaGuinea-BissauGuyanaHaitiHeard and Mcdonald IslandsHoly See (Vatican City State)HondurasHong Kong, SAR ChinaHungaryIcelandIndiaIndonesiaIraqIrelandIsle of ManIsraelITJamaicaJapanJerseyJordanKazakhstanKenyaKiribatiKorea (South)KuwaitKyrgyzstanLao PDRLatviaLebanonLesothoLiberiaLibyaLiechtensteinLithuaniaLuxembourgMacao, SAR ChinaMacedonia, Republic ofMadagascarMalawiMalaysiaMaldivesMaliMaltaMarshall IslandsMartiniqueMauritaniaMauritiusMayotteMexicoMicronesia, Federated States ofMoldovaMonacoMongoliaMontenegroMontserratMoroccoMozambiqueMyanmarNamibiaNauruNepalNetherlandsNetherlands AntillesNew CaledoniaNew ZealandNicaraguaNigerNigeriaNiueNorfolk IslandNorthern Mariana IslandsNorwayOmanPakistanPalauPalestinian TerritoryPanamaPapua New GuineaParaguayPeruPhilippinesPitcairnPolandPortugalPuerto RicoQatarRomaniaRwandaRéunionSaint HelenaSaint Kitts and NevisSaint LuciaSaint Pierre and MiquelonSaint Vincent and GrenadinesSaint-BarthélemySaint-Martin (French part)SamoaSan MarinoSao Tome and PrincipeSaudi ArabiaSenegalSerbiaSeychellesSierra LeoneSingaporeSint Maarten (Dutch part)SlovakiaSloveniaSolomon IslandsSouth AfricaSouth Georgia and the South Sandwich IslandsSouth SudanSpainSri LankaSurinameSvalbard and Jan Mayen IslandsSwazilandSwedenSwitzerlandTaiwan, Republic of ChinaTajikistanTanzania, United Republic ofThailandTimor-LesteTogoTokelauTongaTrinidad and TobagoTunisiaTurkeyTurks and Caicos IslandsTuvaluUgandaUkraineUnited Arab EmiratesUnited KingdomUnited States of AmericaUruguayUS Minor Outlying IslandsUzbekistanVanuatuVenezuela (Bolivarian Republic)Viet NamVirgin Islands, USWallis and Futuna IslandsWestern SaharaZambiaZimbabwe

* I have read and agree with the [Privacy policy](https://tools.techidaily.com/abbyy/products/) and the [Cookie policy](https://tools.techidaily.com/abbyy/products/).\*

* I agree to receive email updates from ABBYY Solutions Ltd. such as news related to ABBYY Solutions Ltd. products and technologies, invitations to events and webinars, and information about whitepapers and content related to ABBYY Solutions Ltd. products and services.  
    
I am aware that my consent could be revoked at any time by clicking the unsubscribe link inside any email received from ABBYY Solutions Ltd. or via [ABBYY Data Subject Access Rights Form](https://tools.techidaily.com/abbyy/products/).

Referrer

Query string

GA Client ID

UTM Campaign Name

UTM Source

UTM Medium

UTM Content

ITM Source

Page URL

Captcha Score

Connect with us

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://eaxpv-info.techidaily.com/updated-in-2024-how-to-skip-the-slip-ups-the-8-must-avoid-mistakes-for-new-youtube-stars/"><u>[Updated] In 2024, How to Skip the Slip-Ups The 8 Must-Avoid Mistakes for New YouTube Stars</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/updated-reach-new-heights-on-igtv-top-tactics-for-expanding-your-audience-for-2024/"><u>[Updated] Reach New Heights on IGTV Top Tactics for Expanding Your Audience for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/apples-newest-contenders-how-does-the-m3-macbook-air-stack-up-against-its-predecessor-the-m2-tech-analysis/"><u>Apple's Newest Contenders: How Does the M3 MacBook Air Stack Up Against Its Predecessor, The M2? | Tech Analysis</u></a></li>
<li><a href="https://facebook.techidaily.com/1719151766914-breaking-down-barriers-to-private-conversations-facebooks-revolutionary-end-to-end-encrypted-services-rollout-for-messenger-and-instagram/"><u>Breaking Down Barriers to Private Conversations: Facebook's Revolutionary End-to-End Encrypted Services Rollout for Messenger and Instagram.</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/how-xiaomi-14-mirror-screen-to-pc-drfone-by-drfone-android/"><u>How Xiaomi 14 Mirror Screen to PC? | Dr.fone</u></a></li>
<li><a href="https://android-unlock.techidaily.com/in-2024-top-10-password-cracking-tools-for-lava-blaze-pro-5g-by-drfone-android/"><u>In 2024, Top 10 Password Cracking Tools For Lava Blaze Pro 5G</u></a></li>
<li><a href="https://some-tips.techidaily.com/ios-18-transforms-iphone-14-into-a-creative-powerhouse-for-seamless-content-making-insights-from-zdnet/"><u>IOS 18 Transforms iPhone 14 Into a Creative Powerhouse for Seamless Content Making - Insights From ZDNet</u></a></li>
<li><a href="https://win-howtos.techidaily.com/keyboard-acts-erratically/"><u>Keyboard Acts Erratically</u></a></li>
<li><a href="https://some-tips.techidaily.com/mastering-the-apple-watch-factory-reset-complete-tutorial-by-zdnet/"><u>Mastering the Apple Watch Factory Reset - Complete Tutorial by ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/most-popular-kid-friendly-tablets-as-voted-by-moms-and-dads/"><u>Most Popular Kid-Friendly Tablets as Voted by Moms and Dads</u></a></li>
<li><a href="https://sound-tweaking.techidaily.com/new-in-2024-5-top-audio-tools-to-master-recording-your-voice-with-ease/"><u>New In 2024, 5 Top Audio Tools to Master Recording Your Voice with Ease</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/the-ultimate-guide-to-fitbit-versa-lite-smartwatch-for-enhanced-workouts-at-great-prices/"><u>The Ultimate Guide to Fitbit Versa Lite: Smartwatch for Enhanced Workouts at Great Prices</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/top-10-timeless-family-adventures-on-screen-this-season-for-2024/"><u>Top 10 Timeless Family Adventures on Screen This Season for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-rated-stylus-tablets-in-depth-analysis-and-reviews-by-tech-experts/"><u>Top-Rated Stylus Tablets : In-Depth Analysis & Reviews by Tech Experts</u></a></li>
</ul></div>

