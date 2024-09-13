---
title: Enhance Your Marketing Strategy Using Cookiebot Solutions
date: 2024-09-12T07:16:22.916Z
updated: 2024-09-13T07:16:22.916Z
categories:
  - abbyy
thumbnail: https://thmb.techidaily.com/a65a2d3fb958e05df694286812a1e2454a9d6c6ff463421241eb49561be7ce4c.jpg
---

## Enhance Your Marketing Strategy Using Cookiebot Solutions

[Back to The Intelligent Enterprise](https://tools.techidaily.com/abbyy/products/)

<!-- affiliate ads begin -->
<span id="1977020">
					<video width="128" height="480" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1977020.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1977020">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1977020.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:80px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1977020%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1977020/22993" style="position:absolute;visibility:hidden;" border="0" />
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
<span id="1977032">
					<video width="128" height="480" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1977032.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1977032">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1977032.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:80px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1977032%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1977032/22993" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://snapchat-videos.techidaily.com/new-captivating-chats-with-animated-content-an-in-depth-guide-to-snapchats-gif-feature/"><u>[New] Captivating Chats with Animated Content An In-Depth Guide to Snapchat's GIF Feature</u></a></li>
<li><a href="https://eaxpv-info.techidaily.com/new-in-2024-growth-in-focus-building-a-foundation-of-youtube-backlinks/"><u>[New] In 2024, Growth in Focus Building a Foundation of YouTube Backlinks</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/new-in-2024-navigating-the-past-accelerated-access-to-archived-content/"><u>[New] In 2024, Navigating the Past Accelerated Access to Archived Content</u></a></li>
<li><a href="https://article-tips.techidaily.com/updated-2024-approved-premium-settings-for-virtual-broadcasts/"><u>[Updated] 2024 Approved Premium Settings for Virtual Broadcasts</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/updated-simplifying-the-screen-recording-process-for-dell-users-for-2024/"><u>[Updated] Simplifying the Screen-Recording Process for Dell Users for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/a-walk-down-memory-lane-rediscovering-our-love-for-dial-up-connections-and-their-quirks/"><u>A Walk Down Memory Lane: Rediscovering Our Love for Dial-Up Connections and Their Quirks</u></a></li>
<li><a href="https://some-tips.techidaily.com/discovering-evolution-in-management-tools-how-windows-11-transforms-the-classic-task-manager/"><u>Discovering Evolution in Management Tools: How Windows 11 Transforms the Classic Task Manager</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-your-pcs-creativity-with-advanced-ai-powered-image-generation/"><u>Enhance Your PC's Creativity with Advanced AI-Powered Image Generation</u></a></li>
<li><a href="https://techtrends.techidaily.com/how-to-quick-and-simple-ways-to-take-a-capture-of-your-screen/"><u>How To: Quick & Simple Ways to Take a Capture of Your Screen</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-fake-the-location-to-get-around-the-mlb-blackouts-on-realme-c33-2023-drfone-by-drfone-virtual-android/"><u>In 2024, Fake the Location to Get Around the MLB Blackouts on Realme C33 2023 | Dr.fone</u></a></li>
<li><a href="https://apple-account.techidaily.com/in-2024-turning-off-two-factor-authentication-on-apple-iphone-se-5-tips-you-must-know-by-drfone-ios/"><u>In 2024, Turning Off Two Factor Authentication On Apple iPhone SE? 5 Tips You Must Know</u></a></li>
<li><a href="https://voice-adjusting.techidaily.com/new-in-2024-melody-and-motion-best-sync-videography-applications-of-the-decades-first-half/"><u>New In 2024, Melody and Motion Best-Sync Videography Applications of the Decades First Half</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-7-essential-windows-features-to-activate-for-optimal-performance-the-why-and-how/"><u>Top 7 Essential Windows Features to Activate for Optimal Performance: The Why and How</u></a></li>
<li><a href="https://some-tips.techidaily.com/understanding-quicktime-the-complete-guide-to-apples-media-player/"><u>Understanding QuickTime: The Complete Guide to Apple's Media Player</u></a></li>
<li><a href="https://some-tips.techidaily.com/unintended-hp-printer-software-updates-how-theyre-auto-installing-on-windows-computers/"><u>Unintended HP Printer Software Updates: How They're Auto-Installing on Windows Computers</u></a></li>
</ul></div>

