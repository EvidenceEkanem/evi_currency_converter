<template>
     <div class="main-content">
            <section class="header">
                <div class="container">
                    <div class="converter">
                        <h1>Evidoski Currency Converter</h1>
                        <h2>All actual world currencies live rates, reference information, currency calculator.</h2>
                        <div class="convert-box">
                            <div class="row">
                                <div class="col-md-5 col-sm-12 col-xs-12">
                                    <label class="label">From</label>
                                    <div class="select">
                                        <div class="input-wrap">
                                            <input class="form-control" type="number" :click="getCurrencyNames()"  v-model="amount" value="1" name="finpt" id="finpt">
                                        </div>
                                        <select id="fromCurrency" name="fromCurrency" v-model="fromCurrency"  data-show-subtext="true" class="selectpicker bs-select form-control" data-live-search="true" data-size="8">
                                                                                            <option data-content="<img class='flag' src='/img/flags/AE.png'> <span class='currency_code'>AED</span> <span class='currency_name'>United Arab Emirates Dirham</span>" 
                                                 value="AED">AED</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AF.png'> <span class='currency_code'>AFN</span> <span class='currency_name'>Afghan Afghani</span>" 
                                                 value="AFN">AFN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AL.png'> <span class='currency_code'>ALL</span> <span class='currency_name'>Albanian Lek</span>" 
                                                 value="ALL">ALL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AM.png'> <span class='currency_code'>AMD</span> <span class='currency_name'>Armenian Dram</span>" 
                                                 value="AMD">AMD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AN.png'> <span class='currency_code'>ANG</span> <span class='currency_name'>Netherlands Antillean Guilder</span>" 
                                                 value="ANG">ANG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AO.png'> <span class='currency_code'>AOA</span> <span class='currency_name'>Angolan Kwanza</span>" 
                                                 value="AOA">AOA</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AR.png'> <span class='currency_code'>ARS</span> <span class='currency_name'>Argentine Peso</span>" 
                                                 value="ARS">ARS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AU.png'> <span class='currency_code'>AUD</span> <span class='currency_name'>Australian Dollar</span>" 
                                                 value="AUD">AUD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AW.png'> <span class='currency_code'>AWG</span> <span class='currency_name'>Aruban Florin</span>" 
                                                 value="AWG">AWG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AZ.png'> <span class='currency_code'>AZN</span> <span class='currency_name'>Azerbaijanian Manat</span>" 
                                                 value="AZN">AZN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BA.png'> <span class='currency_code'>BAM</span> <span class='currency_name'>Convertible Mark</span>" 
                                                 value="BAM">BAM</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BB.png'> <span class='currency_code'>BBD</span> <span class='currency_name'>Barbados Dollar</span>" 
                                                 value="BBD">BBD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BD.png'> <span class='currency_code'>BDT</span> <span class='currency_name'>Bangladeshi Taka</span>" 
                                                 value="BDT">BDT</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BG.png'> <span class='currency_code'>BGN</span> <span class='currency_name'>Bulgarian Lev</span>" 
                                                 value="BGN">BGN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BH.png'> <span class='currency_code'>BHD</span> <span class='currency_name'>Bahraini Dinar</span>" 
                                                 value="BHD">BHD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BI.png'> <span class='currency_code'>BIF</span> <span class='currency_name'>Burundi Franc</span>" 
                                                 value="BIF">BIF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BM.png'> <span class='currency_code'>BMD</span> <span class='currency_name'>Bermudian Dollar</span>" 
                                                 value="BMD">BMD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BN.png'> <span class='currency_code'>BND</span> <span class='currency_name'>Brunei Dollar</span>" 
                                                 value="BND">BND</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BO.png'> <span class='currency_code'>BOB</span> <span class='currency_name'>Boliviano</span>" 
                                                 value="BOB">BOB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BR.png'> <span class='currency_code'>BRL</span> <span class='currency_name'>Brazilian Real</span>" 
                                                 value="BRL">BRL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BS.png'> <span class='currency_code'>BSD</span> <span class='currency_name'>Bahamian Dollar</span>" 
                                                 value="BSD">BSD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BTC.png'> <span class='currency_code'>BTC</span> <span class='currency_name'>Bitcoin</span>" 
                                                 value="BTC">BTC</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BT.png'> <span class='currency_code'>BTN</span> <span class='currency_name'>Bhutanese Ngultrum</span>" 
                                                 value="BTN">BTN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BW.png'> <span class='currency_code'>BWP</span> <span class='currency_name'>Botswana Pula</span>" 
                                                 value="BWP">BWP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BY.png'> <span class='currency_code'>BYN</span> <span class='currency_name'>Belarussian Ruble</span>" 
                                                 value="BYN">BYN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BZ.png'> <span class='currency_code'>BZD</span> <span class='currency_name'>Belize Dollar</span>" 
                                                 value="BZD">BZD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CA.png'> <span class='currency_code'>CAD</span> <span class='currency_name'>Canadian Dollar</span>" 
                                                 value="CAD">CAD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CD.png'> <span class='currency_code'>CDF</span> <span class='currency_name'>Congolese Franc</span>" 
                                                 value="CDF">CDF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CH.png'> <span class='currency_code'>CHF</span> <span class='currency_name'>Swiss Franc</span>" 
                                                 value="CHF">CHF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CL.png'> <span class='currency_code'>CLP</span> <span class='currency_name'>Chilean Peso</span>" 
                                                 value="CLP">CLP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CN.png'> <span class='currency_code'>CNY</span> <span class='currency_name'>Chinese Yuan</span>" 
                                                 value="CNY">CNY</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CO.png'> <span class='currency_code'>COP</span> <span class='currency_name'>Colombian Peso</span>" 
                                                 value="COP">COP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CR.png'> <span class='currency_code'>CRC</span> <span class='currency_name'>Costa Rican Colon</span>" 
                                                 value="CRC">CRC</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CU.png'> <span class='currency_code'>CUP</span> <span class='currency_name'>Cuban Peso</span>" 
                                                 value="CUP">CUP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CV.png'> <span class='currency_code'>CVE</span> <span class='currency_name'>Cabo Verde Escudo</span>" 
                                                 value="CVE">CVE</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CZ.png'> <span class='currency_code'>CZK</span> <span class='currency_name'>Czech Koruna</span>" 
                                                 value="CZK">CZK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/DJ.png'> <span class='currency_code'>DJF</span> <span class='currency_name'>Djibouti Franc</span>" 
                                                 value="DJF">DJF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/DK.png'> <span class='currency_code'>DKK</span> <span class='currency_name'>Danish Krone</span>" 
                                                 value="DKK">DKK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/DO.png'> <span class='currency_code'>DOP</span> <span class='currency_name'>Dominican Peso</span>" 
                                                 value="DOP">DOP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/DZ.png'> <span class='currency_code'>DZD</span> <span class='currency_name'>Algerian Dinar</span>" 
                                                 value="DZD">DZD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/EG.png'> <span class='currency_code'>EGP</span> <span class='currency_name'>Egyptian Pound</span>" 
                                                 value="EGP">EGP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ER.png'> <span class='currency_code'>ERN</span> <span class='currency_name'>Eritrean Nakfa</span>" 
                                                 value="ERN">ERN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ET.png'> <span class='currency_code'>ETB</span> <span class='currency_name'>Ethiopian Birr</span>" 
                                                 value="ETB">ETB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/EU.png'> <span class='currency_code'>EUR</span> <span class='currency_name'>Euro</span>" 
                                                 value="EUR">EUR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/FJ.png'> <span class='currency_code'>FJD</span> <span class='currency_name'>Fiji Dollar</span>" 
                                                 value="FJD">FJD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/FK.png'> <span class='currency_code'>FKP</span> <span class='currency_name'>Falkland Islands Pound</span>" 
                                                 value="FKP">FKP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GB.png'> <span class='currency_code'>GBP</span> <span class='currency_name'>British Pound</span>" 
                                                 value="GBP">GBP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GE.png'> <span class='currency_code'>GEL</span> <span class='currency_name'>Georgian Lari</span>" 
                                                 value="GEL">GEL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GG.png'> <span class='currency_code'>GGP</span> <span class='currency_name'>Guernsey Pound</span>" 
                                                 value="GGP">GGP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GH.png'> <span class='currency_code'>GHS</span> <span class='currency_name'>Ghana Cedi</span>" 
                                                 value="GHS">GHS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GI.png'> <span class='currency_code'>GIP</span> <span class='currency_name'>Gibraltar Pound</span>" 
                                                 value="GIP">GIP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GM.png'> <span class='currency_code'>GMD</span> <span class='currency_name'>Gambian Dalasi</span>" 
                                                 value="GMD">GMD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GN.png'> <span class='currency_code'>GNF</span> <span class='currency_name'>Guinea Franc</span>" 
                                                 value="GNF">GNF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GT.png'> <span class='currency_code'>GTQ</span> <span class='currency_name'>Guatemalan Quetzal</span>" 
                                                 value="GTQ">GTQ</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GY.png'> <span class='currency_code'>GYD</span> <span class='currency_name'>Guyana Dollar</span>" 
                                                 value="GYD">GYD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HK.png'> <span class='currency_code'>HKD</span> <span class='currency_name'>Hong Kong Dollar</span>" 
                                                 value="HKD">HKD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HN.png'> <span class='currency_code'>HNL</span> <span class='currency_name'>Honduran Lempira</span>" 
                                                 value="HNL">HNL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HR.png'> <span class='currency_code'>HRK</span> <span class='currency_name'>Croatian Kuna</span>" 
                                                 value="HRK">HRK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HT.png'> <span class='currency_code'>HTG</span> <span class='currency_name'>Haitian Gourde</span>" 
                                                 value="HTG">HTG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HU.png'> <span class='currency_code'>HUF</span> <span class='currency_name'>Hungarian Forint</span>" 
                                                 value="HUF">HUF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ID.png'> <span class='currency_code'>IDR</span> <span class='currency_name'>Indonesian Rupiah</span>" 
                                                 value="IDR">IDR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IL.png'> <span class='currency_code'>ILS</span> <span class='currency_name'>Israeli Shekel</span>" 
                                                 value="ILS">ILS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IN.png'> <span class='currency_code'>INR</span> <span class='currency_name'>Indian Rupee</span>" 
                                                 value="INR">INR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IQ.png'> <span class='currency_code'>IQD</span> <span class='currency_name'>Iraqi Dinar</span>" 
                                                 value="IQD">IQD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IR.png'> <span class='currency_code'>IRR</span> <span class='currency_name'>Iranian Rial</span>" 
                                                 value="IRR">IRR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IS.png'> <span class='currency_code'>ISK</span> <span class='currency_name'>Iceland Krona</span>" 
                                                 value="ISK">ISK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/JE.png'> <span class='currency_code'>JEP</span> <span class='currency_name'>Jersey Pound</span>" 
                                                 value="JEP">JEP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/JM.png'> <span class='currency_code'>JMD</span> <span class='currency_name'>Jamaican Dollar</span>" 
                                                 value="JMD">JMD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/JO.png'> <span class='currency_code'>JOD</span> <span class='currency_name'>Jordanian Dinar</span>" 
                                                 value="JOD">JOD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/JP.png'> <span class='currency_code'>JPY</span> <span class='currency_name'>Japanese Yen</span>" 
                                                 value="JPY">JPY</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KE.png'> <span class='currency_code'>KES</span> <span class='currency_name'>Kenyan Shilling</span>" 
                                                 value="KES">KES</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KG.png'> <span class='currency_code'>KGS</span> <span class='currency_name'>Kyrgyzstani Som</span>" 
                                                 value="KGS">KGS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KH.png'> <span class='currency_code'>KHR</span> <span class='currency_name'>Cambodian Riel</span>" 
                                                 value="KHR">KHR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KM.png'> <span class='currency_code'>KMF</span> <span class='currency_name'>Comoro Franc</span>" 
                                                 value="KMF">KMF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KP.png'> <span class='currency_code'>KPW</span> <span class='currency_name'>North Korean Won</span>" 
                                                 value="KPW">KPW</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KR.png'> <span class='currency_code'>KRW</span> <span class='currency_name'>South Korean Won</span>" 
                                                 value="KRW">KRW</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KW.png'> <span class='currency_code'>KWD</span> <span class='currency_name'>Kuwaiti Dinar</span>" 
                                                 value="KWD">KWD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KY.png'> <span class='currency_code'>KYD</span> <span class='currency_name'>Cayman Islands Dollar</span>" 
                                                 value="KYD">KYD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KZ.png'> <span class='currency_code'>KZT</span> <span class='currency_name'>Kazakhstani Tenge</span>" 
                                                 value="KZT">KZT</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LA.png'> <span class='currency_code'>LAK</span> <span class='currency_name'>Lao Kip</span>" 
                                                 value="LAK">LAK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LB.png'> <span class='currency_code'>LBP</span> <span class='currency_name'>Lebanese Pound</span>" 
                                                 value="LBP">LBP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LK.png'> <span class='currency_code'>LKR</span> <span class='currency_name'>Sri Lanka Rupee</span>" 
                                                 value="LKR">LKR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LR.png'> <span class='currency_code'>LRD</span> <span class='currency_name'>Liberian Dollar</span>" 
                                                 value="LRD">LRD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LS.png'> <span class='currency_code'>LSL</span> <span class='currency_name'>Lesotho Loti</span>" 
                                                 value="LSL">LSL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LY.png'> <span class='currency_code'>LYD</span> <span class='currency_name'>Libyan Dinar</span>" 
                                                 value="LYD">LYD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MA.png'> <span class='currency_code'>MAD</span> <span class='currency_name'>Moroccan Dirham</span>" 
                                                 value="MAD">MAD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MD.png'> <span class='currency_code'>MDL</span> <span class='currency_name'>Moldovan Leu</span>" 
                                                 value="MDL">MDL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MG.png'> <span class='currency_code'>MGA</span> <span class='currency_name'>Malagasy Ariary</span>" 
                                                 value="MGA">MGA</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MK.png'> <span class='currency_code'>MKD</span> <span class='currency_name'>Macedonian Denar</span>" 
                                                 value="MKD">MKD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MM.png'> <span class='currency_code'>MMK</span> <span class='currency_name'>Myanmar Kyat</span>" 
                                                 value="MMK">MMK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MN.png'> <span class='currency_code'>MNT</span> <span class='currency_name'>Mongolian Tugrik</span>" 
                                                 value="MNT">MNT</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MO.png'> <span class='currency_code'>MOP</span> <span class='currency_name'>Macanese Pataca</span>" 
                                                 value="MOP">MOP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MR.png'> <span class='currency_code'>MRO</span> <span class='currency_name'>Mauritanian Ouguiya</span>" 
                                                 value="MRO">MRO</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MU.png'> <span class='currency_code'>MUR</span> <span class='currency_name'>Mauritius Rupee</span>" 
                                                 value="MUR">MUR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MV.png'> <span class='currency_code'>MVR</span> <span class='currency_name'>Maldivian Rufiyaa</span>" 
                                                 value="MVR">MVR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MW.png'> <span class='currency_code'>MWK</span> <span class='currency_name'>Malawian Kwacha</span>" 
                                                 value="MWK">MWK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MX.png'> <span class='currency_code'>MXN</span> <span class='currency_name'>Mexican Peso</span>" 
                                                 value="MXN">MXN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MY.png'> <span class='currency_code'>MYR</span> <span class='currency_name'>Malaysian Ringgit</span>" 
                                                 value="MYR">MYR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MZ.png'> <span class='currency_code'>MZN</span> <span class='currency_name'>Mozambique Metical</span>" 
                                                 value="MZN">MZN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NA.png'> <span class='currency_code'>NAD</span> <span class='currency_name'>Namibia Dollar</span>" 
                                                 value="NAD">NAD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NG.png'> <span class='currency_code'>NGN</span> <span class='currency_name'>Nigerian Naira</span>" 
                                                 value="NGN">NGN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NI.png'> <span class='currency_code'>NIO</span> <span class='currency_name'>Cordoba Oro</span>" 
                                                 value="NIO">NIO</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NO.png'> <span class='currency_code'>NOK</span> <span class='currency_name'>Norwegian Krone</span>" 
                                                 value="NOK">NOK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NP.png'> <span class='currency_code'>NPR</span> <span class='currency_name'>Nepalese Rupee</span>" 
                                                 value="NPR">NPR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NZ.png'> <span class='currency_code'>NZD</span> <span class='currency_name'>New Zealand Dollar</span>" 
                                                 value="NZD">NZD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/OM.png'> <span class='currency_code'>OMR</span> <span class='currency_name'>Rial Omani</span>" 
                                                 value="OMR">OMR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PA.png'> <span class='currency_code'>PAB</span> <span class='currency_name'>Panamanian Balboa</span>" 
                                                 value="PAB">PAB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PE.png'> <span class='currency_code'>PEN</span> <span class='currency_name'>Peruvian Sol</span>" 
                                                 value="PEN">PEN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PG.png'> <span class='currency_code'>PGK</span> <span class='currency_name'>Papua New Guinean Kina</span>" 
                                                 value="PGK">PGK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PH.png'> <span class='currency_code'>PHP</span> <span class='currency_name'>Philippine Peso</span>" 
                                                 value="PHP">PHP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PK.png'> <span class='currency_code'>PKR</span> <span class='currency_name'>Pakistani Rupee</span>" 
                                                 value="PKR">PKR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PL.png'> <span class='currency_code'>PLN</span> <span class='currency_name'>Polish Zloty</span>" 
                                                 value="PLN">PLN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PY.png'> <span class='currency_code'>PYG</span> <span class='currency_name'>Paraguayan Guarani</span>" 
                                                 value="PYG">PYG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/QA.png'> <span class='currency_code'>QAR</span> <span class='currency_name'>Qatari Rial</span>" 
                                                 value="QAR">QAR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/RO.png'> <span class='currency_code'>RON</span> <span class='currency_name'>Romanian Leu</span>" 
                                                 value="RON">RON</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/RS.png'> <span class='currency_code'>RSD</span> <span class='currency_name'>Serbian Dinar</span>" 
                                                 value="RSD">RSD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/RU.png'> <span class='currency_code'>RUB</span> <span class='currency_name'>Russian Ruble</span>" 
                                                 value="RUB">RUB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/RW.png'> <span class='currency_code'>RWF</span> <span class='currency_name'>Rwanda Franc</span>" 
                                                 value="RWF">RWF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SA.png'> <span class='currency_code'>SAR</span> <span class='currency_name'>Saudi Riyal</span>" 
                                                 value="SAR">SAR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SB.png'> <span class='currency_code'>SBD</span> <span class='currency_name'>Solomon Islands Dollar</span>" 
                                                 value="SBD">SBD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SC.png'> <span class='currency_code'>SCR</span> <span class='currency_name'>Seychelles Rupee</span>" 
                                                 value="SCR">SCR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SD.png'> <span class='currency_code'>SDG</span> <span class='currency_name'>Sudanese Pound</span>" 
                                                 value="SDG">SDG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SE.png'> <span class='currency_code'>SEK</span> <span class='currency_name'>Swedish Krona</span>" 
                                                 value="SEK">SEK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SG.png'> <span class='currency_code'>SGD</span> <span class='currency_name'>Singapore Dollar</span>" 
                                                 value="SGD">SGD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SH.png'> <span class='currency_code'>SHP</span> <span class='currency_name'>Saint Helena Pound</span>" 
                                                 value="SHP">SHP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SL.png'> <span class='currency_code'>SLL</span> <span class='currency_name'>Sierra Leonean Leone</span>" 
                                                 value="SLL">SLL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SO.png'> <span class='currency_code'>SOS</span> <span class='currency_name'>Somali Shilling</span>" 
                                                 value="SOS">SOS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SR.png'> <span class='currency_code'>SRD</span> <span class='currency_name'>Surinam Dollar</span>" 
                                                 value="SRD">SRD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ST.png'> <span class='currency_code'>STD</span> <span class='currency_name'>Sao Tomean Dobra</span>" 
                                                 value="STD">STD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SV.png'> <span class='currency_code'>SVC</span> <span class='currency_name'>El Salvador Colon</span>" 
                                                 value="SVC">SVC</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SY.png'> <span class='currency_code'>SYP</span> <span class='currency_name'>Syrian Pound</span>" 
                                                 value="SYP">SYP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SZ.png'> <span class='currency_code'>SZL</span> <span class='currency_name'>Swazi Lilangeni</span>" 
                                                 value="SZL">SZL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TH.png'> <span class='currency_code'>THB</span> <span class='currency_name'>Thai Baht</span>" 
                                                 value="THB">THB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TJ.png'> <span class='currency_code'>TJS</span> <span class='currency_name'>Tajikistani Somoni</span>" 
                                                 value="TJS">TJS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TM.png'> <span class='currency_code'>TMT</span> <span class='currency_name'>Turkmenistan New Manat</span>" 
                                                 value="TMT">TMT</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TN.png'> <span class='currency_code'>TND</span> <span class='currency_name'>Tunisian Dinar</span>" 
                                                 value="TND">TND</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TO.png'> <span class='currency_code'>TOP</span> <span class='currency_name'>Tongan Pa'anga</span>" 
                                                 value="TOP">TOP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TR.png'> <span class='currency_code'>TRY</span> <span class='currency_name'>Turkish Lira</span>" 
                                                 value="TRY">TRY</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TT.png'> <span class='currency_code'>TTD</span> <span class='currency_name'>Trinidad and Tobago Dollar</span>" 
                                                 value="TTD">TTD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TW.png'> <span class='currency_code'>TWD</span> <span class='currency_name'>New Taiwan Dollar</span>" 
                                                 value="TWD">TWD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TZ.png'> <span class='currency_code'>TZS</span> <span class='currency_name'>Tanzanian Shilling</span>" 
                                                 value="TZS">TZS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/UA.png'> <span class='currency_code'>UAH</span> <span class='currency_name'>Ukrainian Hryvnia</span>" 
                                                 value="UAH">UAH</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/UG.png'> <span class='currency_code'>UGX</span> <span class='currency_name'>Uganda Shilling</span>" 
                                                 value="UGX">UGX</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/US.png'> <span class='currency_code'>USD</span> <span class='currency_name'>United States Dollar</span>" 
                                                 value="USD">USD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/UY.png'> <span class='currency_code'>UYU</span> <span class='currency_name'>Peso Uruguayo</span>" 
                                                 value="UYU">UYU</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/UZ.png'> <span class='currency_code'>UZS</span> <span class='currency_name'>Uzbekistan Sum</span>" 
                                                 value="UZS">UZS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/VE.png'> <span class='currency_code'>VEF</span> <span class='currency_name'>Venezuelan Bolivar</span>" 
                                                 value="VEF">VEF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/VN.png'> <span class='currency_code'>VND</span> <span class='currency_name'>Vietnamese Dong</span>" 
                                                 value="VND">VND</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/VU.png'> <span class='currency_code'>VUV</span> <span class='currency_name'>Vanuatu Vatu</span>" 
                                                 value="VUV">VUV</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/WS.png'> <span class='currency_code'>WST</span> <span class='currency_name'>Samoan Tala</span>" 
                                                 value="WST">WST</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CF.png'> <span class='currency_code'>XAF</span> <span class='currency_name'>CFA Franc BEAC</span>" 
                                                 value="XAF">XAF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/_unknown.png'> <span class='currency_code'>XCD</span> <span class='currency_name'>East Caribbean Dollar</span>" 
                                                 value="XCD">XCD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/_unknown.png'> <span class='currency_code'>XOF</span> <span class='currency_name'>CFA Franc BCEAO</span>" 
                                                 value="XOF">XOF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/_unknown.png'> <span class='currency_code'>XPF</span> <span class='currency_name'>CFP Franc</span>" 
                                                 value="XPF">XPF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/YE.png'> <span class='currency_code'>YER</span> <span class='currency_name'>Yemeni Rial</span>" 
                                                 value="YER">YER</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ZA.png'> <span class='currency_code'>ZAR</span> <span class='currency_name'>South African Rand</span>" 
                                                 value="ZAR">ZAR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ZM.png'> <span class='currency_code'>ZMW</span> <span class='currency_name'>Zambian Kwacha</span>" 
                                                 value="ZMW">ZMW</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ZW.png'> <span class='currency_code'>ZWL</span> <span class='currency_name'>Zimbabwean Dollar</span>" 
                                                 value="ZWL">ZWL</option>
                                                                                                </select>
                                    </div>
                                </div>
                                <div class="col-md-2 col-sm-12 col-xs-12">
                                    <label class="label"><br /></label>
                                    <div class="select text-center">
                                        <button :click="convertCurrencyBackward()" class="exchange-btn">
                                            <i class="fa fa-refresh text-white" style="font-size:24px"></i>
                                        </button>
                                    </div>
                                </div>
                                <div class="col-md-5 col-sm-12 col-xs-12">
                                    <label class="label">To</label>
                                    <div class="select">
                                        <div class="input-wrap">
                                            <input class="form-control" type="number" v-model="reversedAmount" name="tinpt" id="tinpt">
                                        </div>
                                        <select id="toCurrency" name="toCurrency" v-model="toCurrency" :click="convertCurrency()"  data-show-subtext="true" class="selectpicker bs-select form-control" data-live-search="true" data-size="8">
                                                                          n                  <option data-content="<img class='flag' src='/img/flags/AE.png'> <span class='currency_code'>AED</span> <span class='currency_name'>United Arab Emirates Dirham</span>" 
                                                 value="AED">AED</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AF.png'> <span class='currency_code'>AFN</span> <span class='currency_name'>Afghan Afghani</span>" 
                                                 value="AFN">AFN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AL.png'> <span class='currency_code'>ALL</span> <span class='currency_name'>Albanian Lek</span>" 
                                                 value="ALL">ALL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AM.png'> <span class='currency_code'>AMD</span> <span class='currency_name'>Armenian Dram</span>" 
                                                 value="AMD">AMD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AN.png'> <span class='currency_code'>ANG</span> <span class='currency_name'>Netherlands Antillean Guilder</span>" 
                                                 value="ANG">ANG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AO.png'> <span class='currency_code'>AOA</span> <span class='currency_name'>Angolan Kwanza</span>" 
                                                 value="AOA">AOA</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AR.png'> <span class='currency_code'>ARS</span> <span class='currency_name'>Argentine Peso</span>" 
                                                 value="ARS">ARS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AU.png'> <span class='currency_code'>AUD</span> <span class='currency_name'>Australian Dollar</span>" 
                                                 value="AUD">AUD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AW.png'> <span class='currency_code'>AWG</span> <span class='currency_name'>Aruban Florin</span>" 
                                                 value="AWG">AWG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/AZ.png'> <span class='currency_code'>AZN</span> <span class='currency_name'>Azerbaijanian Manat</span>" 
                                                 value="AZN">AZN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BA.png'> <span class='currency_code'>BAM</span> <span class='currency_name'>Convertible Mark</span>" 
                                                 value="BAM">BAM</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BB.png'> <span class='currency_code'>BBD</span> <span class='currency_name'>Barbados Dollar</span>" 
                                                 value="BBD">BBD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BD.png'> <span class='currency_code'>BDT</span> <span class='currency_name'>Bangladeshi Taka</span>" 
                                                 value="BDT">BDT</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BG.png'> <span class='currency_code'>BGN</span> <span class='currency_name'>Bulgarian Lev</span>" 
                                                 value="BGN">BGN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BH.png'> <span class='currency_code'>BHD</span> <span class='currency_name'>Bahraini Dinar</span>" 
                                                 value="BHD">BHD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BI.png'> <span class='currency_code'>BIF</span> <span class='currency_name'>Burundi Franc</span>" 
                                                 value="BIF">BIF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BM.png'> <span class='currency_code'>BMD</span> <span class='currency_name'>Bermudian Dollar</span>" 
                                                 value="BMD">BMD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BN.png'> <span class='currency_code'>BND</span> <span class='currency_name'>Brunei Dollar</span>" 
                                                 value="BND">BND</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BO.png'> <span class='currency_code'>BOB</span> <span class='currency_name'>Boliviano</span>" 
                                                 value="BOB">BOB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BR.png'> <span class='currency_code'>BRL</span> <span class='currency_name'>Brazilian Real</span>" 
                                                 value="BRL">BRL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BS.png'> <span class='currency_code'>BSD</span> <span class='currency_name'>Bahamian Dollar</span>" 
                                                 value="BSD">BSD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BTC.png'> <span class='currency_code'>BTC</span> <span class='currency_name'>Bitcoin</span>" 
                                                 value="BTC">BTC</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BT.png'> <span class='currency_code'>BTN</span> <span class='currency_name'>Bhutanese Ngultrum</span>" 
                                                 value="BTN">BTN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BW.png'> <span class='currency_code'>BWP</span> <span class='currency_name'>Botswana Pula</span>" 
                                                 value="BWP">BWP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BY.png'> <span class='currency_code'>BYN</span> <span class='currency_name'>Belarussian Ruble</span>" 
                                                 value="BYN">BYN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/BZ.png'> <span class='currency_code'>BZD</span> <span class='currency_name'>Belize Dollar</span>" 
                                                 value="BZD">BZD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CA.png'> <span class='currency_code'>CAD</span> <span class='currency_name'>Canadian Dollar</span>" 
                                                 value="CAD">CAD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CD.png'> <span class='currency_code'>CDF</span> <span class='currency_name'>Congolese Franc</span>" 
                                                 value="CDF">CDF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CH.png'> <span class='currency_code'>CHF</span> <span class='currency_name'>Swiss Franc</span>" 
                                                 value="CHF">CHF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CL.png'> <span class='currency_code'>CLP</span> <span class='currency_name'>Chilean Peso</span>" 
                                                 value="CLP">CLP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CN.png'> <span class='currency_code'>CNY</span> <span class='currency_name'>Chinese Yuan</span>" 
                                                 value="CNY">CNY</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CO.png'> <span class='currency_code'>COP</span> <span class='currency_name'>Colombian Peso</span>" 
                                                 value="COP">COP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CR.png'> <span class='currency_code'>CRC</span> <span class='currency_name'>Costa Rican Colon</span>" 
                                                 value="CRC">CRC</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CU.png'> <span class='currency_code'>CUP</span> <span class='currency_name'>Cuban Peso</span>" 
                                                 value="CUP">CUP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CV.png'> <span class='currency_code'>CVE</span> <span class='currency_name'>Cabo Verde Escudo</span>" 
                                                 value="CVE">CVE</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CZ.png'> <span class='currency_code'>CZK</span> <span class='currency_name'>Czech Koruna</span>" 
                                                 value="CZK">CZK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/DJ.png'> <span class='currency_code'>DJF</span> <span class='currency_name'>Djibouti Franc</span>" 
                                                 value="DJF">DJF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/DK.png'> <span class='currency_code'>DKK</span> <span class='currency_name'>Danish Krone</span>" 
                                                 value="DKK">DKK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/DO.png'> <span class='currency_code'>DOP</span> <span class='currency_name'>Dominican Peso</span>" 
                                                 value="DOP">DOP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/DZ.png'> <span class='currency_code'>DZD</span> <span class='currency_name'>Algerian Dinar</span>" 
                                                 value="DZD">DZD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/EG.png'> <span class='currency_code'>EGP</span> <span class='currency_name'>Egyptian Pound</span>" 
                                                 value="EGP">EGP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ER.png'> <span class='currency_code'>ERN</span> <span class='currency_name'>Eritrean Nakfa</span>" 
                                                 value="ERN">ERN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ET.png'> <span class='currency_code'>ETB</span> <span class='currency_name'>Ethiopian Birr</span>" 
                                                 value="ETB">ETB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/EU.png'> <span class='currency_code'>EUR</span> <span class='currency_name'>Euro</span>" 
                                                 value="EUR">EUR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/FJ.png'> <span class='currency_code'>FJD</span> <span class='currency_name'>Fiji Dollar</span>" 
                                                 value="FJD">FJD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/FK.png'> <span class='currency_code'>FKP</span> <span class='currency_name'>Falkland Islands Pound</span>" 
                                                 value="FKP">FKP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GB.png'> <span class='currency_code'>GBP</span> <span class='currency_name'>British Pound</span>" 
                                                 value="GBP">GBP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GE.png'> <span class='currency_code'>GEL</span> <span class='currency_name'>Georgian Lari</span>" 
                                                 value="GEL">GEL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GG.png'> <span class='currency_code'>GGP</span> <span class='currency_name'>Guernsey Pound</span>" 
                                                 value="GGP">GGP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GH.png'> <span class='currency_code'>GHS</span> <span class='currency_name'>Ghana Cedi</span>" 
                                                 value="GHS">GHS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GI.png'> <span class='currency_code'>GIP</span> <span class='currency_name'>Gibraltar Pound</span>" 
                                                 value="GIP">GIP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GM.png'> <span class='currency_code'>GMD</span> <span class='currency_name'>Gambian Dalasi</span>" 
                                                 value="GMD">GMD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GN.png'> <span class='currency_code'>GNF</span> <span class='currency_name'>Guinea Franc</span>" 
                                                 value="GNF">GNF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GT.png'> <span class='currency_code'>GTQ</span> <span class='currency_name'>Guatemalan Quetzal</span>" 
                                                 value="GTQ">GTQ</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/GY.png'> <span class='currency_code'>GYD</span> <span class='currency_name'>Guyana Dollar</span>" 
                                                 value="GYD">GYD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HK.png'> <span class='currency_code'>HKD</span> <span class='currency_name'>Hong Kong Dollar</span>" 
                                                 value="HKD">HKD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HN.png'> <span class='currency_code'>HNL</span> <span class='currency_name'>Honduran Lempira</span>" 
                                                 value="HNL">HNL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HR.png'> <span class='currency_code'>HRK</span> <span class='currency_name'>Croatian Kuna</span>" 
                                                 value="HRK">HRK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HT.png'> <span class='currency_code'>HTG</span> <span class='currency_name'>Haitian Gourde</span>" 
                                                 value="HTG">HTG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/HU.png'> <span class='currency_code'>HUF</span> <span class='currency_name'>Hungarian Forint</span>" 
                                                 value="HUF">HUF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ID.png'> <span class='currency_code'>IDR</span> <span class='currency_name'>Indonesian Rupiah</span>" 
                                                 value="IDR">IDR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IL.png'> <span class='currency_code'>ILS</span> <span class='currency_name'>Israeli Shekel</span>" 
                                                 value="ILS">ILS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IN.png'> <span class='currency_code'>INR</span> <span class='currency_name'>Indian Rupee</span>" 
                                                 value="INR">INR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IQ.png'> <span class='currency_code'>IQD</span> <span class='currency_name'>Iraqi Dinar</span>" 
                                                 value="IQD">IQD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IR.png'> <span class='currency_code'>IRR</span> <span class='currency_name'>Iranian Rial</span>" 
                                                 value="IRR">IRR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/IS.png'> <span class='currency_code'>ISK</span> <span class='currency_name'>Iceland Krona</span>" 
                                                 value="ISK">ISK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/JE.png'> <span class='currency_code'>JEP</span> <span class='currency_name'>Jersey Pound</span>" 
                                                 value="JEP">JEP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/JM.png'> <span class='currency_code'>JMD</span> <span class='currency_name'>Jamaican Dollar</span>" 
                                                 value="JMD">JMD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/JO.png'> <span class='currency_code'>JOD</span> <span class='currency_name'>Jordanian Dinar</span>" 
                                                 value="JOD">JOD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/JP.png'> <span class='currency_code'>JPY</span> <span class='currency_name'>Japanese Yen</span>" 
                                                 value="JPY">JPY</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KE.png'> <span class='currency_code'>KES</span> <span class='currency_name'>Kenyan Shilling</span>" 
                                                 value="KES">KES</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KG.png'> <span class='currency_code'>KGS</span> <span class='currency_name'>Kyrgyzstani Som</span>" 
                                                 value="KGS">KGS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KH.png'> <span class='currency_code'>KHR</span> <span class='currency_name'>Cambodian Riel</span>" 
                                                 value="KHR">KHR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KM.png'> <span class='currency_code'>KMF</span> <span class='currency_name'>Comoro Franc</span>" 
                                                 value="KMF">KMF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KP.png'> <span class='currency_code'>KPW</span> <span class='currency_name'>North Korean Won</span>" 
                                                 value="KPW">KPW</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KR.png'> <span class='currency_code'>KRW</span> <span class='currency_name'>South Korean Won</span>" 
                                                 value="KRW">KRW</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KW.png'> <span class='currency_code'>KWD</span> <span class='currency_name'>Kuwaiti Dinar</span>" 
                                                 value="KWD">KWD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KY.png'> <span class='currency_code'>KYD</span> <span class='currency_name'>Cayman Islands Dollar</span>" 
                                                 value="KYD">KYD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/KZ.png'> <span class='currency_code'>KZT</span> <span class='currency_name'>Kazakhstani Tenge</span>" 
                                                 value="KZT">KZT</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LA.png'> <span class='currency_code'>LAK</span> <span class='currency_name'>Lao Kip</span>" 
                                                 value="LAK">LAK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LB.png'> <span class='currency_code'>LBP</span> <span class='currency_name'>Lebanese Pound</span>" 
                                                 value="LBP">LBP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LK.png'> <span class='currency_code'>LKR</span> <span class='currency_name'>Sri Lanka Rupee</span>" 
                                                 value="LKR">LKR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LR.png'> <span class='currency_code'>LRD</span> <span class='currency_name'>Liberian Dollar</span>" 
                                                 value="LRD">LRD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LS.png'> <span class='currency_code'>LSL</span> <span class='currency_name'>Lesotho Loti</span>" 
                                                 value="LSL">LSL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/LY.png'> <span class='currency_code'>LYD</span> <span class='currency_name'>Libyan Dinar</span>" 
                                                 value="LYD">LYD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MA.png'> <span class='currency_code'>MAD</span> <span class='currency_name'>Moroccan Dirham</span>" 
                                                 value="MAD">MAD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MD.png'> <span class='currency_code'>MDL</span> <span class='currency_name'>Moldovan Leu</span>" 
                                                 value="MDL">MDL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MG.png'> <span class='currency_code'>MGA</span> <span class='currency_name'>Malagasy Ariary</span>" 
                                                 value="MGA">MGA</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MK.png'> <span class='currency_code'>MKD</span> <span class='currency_name'>Macedonian Denar</span>" 
                                                 value="MKD">MKD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MM.png'> <span class='currency_code'>MMK</span> <span class='currency_name'>Myanmar Kyat</span>" 
                                                 value="MMK">MMK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MN.png'> <span class='currency_code'>MNT</span> <span class='currency_name'>Mongolian Tugrik</span>" 
                                                 value="MNT">MNT</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MO.png'> <span class='currency_code'>MOP</span> <span class='currency_name'>Macanese Pataca</span>" 
                                                 value="MOP">MOP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MR.png'> <span class='currency_code'>MRO</span> <span class='currency_name'>Mauritanian Ouguiya</span>" 
                                                 value="MRO">MRO</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MU.png'> <span class='currency_code'>MUR</span> <span class='currency_name'>Mauritius Rupee</span>" 
                                                 value="MUR">MUR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MV.png'> <span class='currency_code'>MVR</span> <span class='currency_name'>Maldivian Rufiyaa</span>" 
                                                 value="MVR">MVR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MW.png'> <span class='currency_code'>MWK</span> <span class='currency_name'>Malawian Kwacha</span>" 
                                                 value="MWK">MWK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MX.png'> <span class='currency_code'>MXN</span> <span class='currency_name'>Mexican Peso</span>" 
                                                 value="MXN">MXN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MY.png'> <span class='currency_code'>MYR</span> <span class='currency_name'>Malaysian Ringgit</span>" 
                                                 value="MYR">MYR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/MZ.png'> <span class='currency_code'>MZN</span> <span class='currency_name'>Mozambique Metical</span>" 
                                                 value="MZN">MZN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NA.png'> <span class='currency_code'>NAD</span> <span class='currency_name'>Namibia Dollar</span>" 
                                                 value="NAD">NAD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NG.png'> <span class='currency_code'>NGN</span> <span class='currency_name'>Nigerian Naira</span>" 
                                                 value="NGN">NGN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NI.png'> <span class='currency_code'>NIO</span> <span class='currency_name'>Cordoba Oro</span>" 
                                                 value="NIO">NIO</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NO.png'> <span class='currency_code'>NOK</span> <span class='currency_name'>Norwegian Krone</span>" 
                                                 value="NOK">NOK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NP.png'> <span class='currency_code'>NPR</span> <span class='currency_name'>Nepalese Rupee</span>" 
                                                 value="NPR">NPR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/NZ.png'> <span class='currency_code'>NZD</span> <span class='currency_name'>New Zealand Dollar</span>" 
                                                 value="NZD">NZD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/OM.png'> <span class='currency_code'>OMR</span> <span class='currency_name'>Rial Omani</span>" 
                                                 value="OMR">OMR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PA.png'> <span class='currency_code'>PAB</span> <span class='currency_name'>Panamanian Balboa</span>" 
                                                 value="PAB">PAB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PE.png'> <span class='currency_code'>PEN</span> <span class='currency_name'>Peruvian Sol</span>" 
                                                 value="PEN">PEN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PG.png'> <span class='currency_code'>PGK</span> <span class='currency_name'>Papua New Guinean Kina</span>" 
                                                 value="PGK">PGK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PH.png'> <span class='currency_code'>PHP</span> <span class='currency_name'>Philippine Peso</span>" 
                                                 value="PHP">PHP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PK.png'> <span class='currency_code'>PKR</span> <span class='currency_name'>Pakistani Rupee</span>" 
                                                 value="PKR">PKR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PL.png'> <span class='currency_code'>PLN</span> <span class='currency_name'>Polish Zloty</span>" 
                                                 value="PLN">PLN</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/PY.png'> <span class='currency_code'>PYG</span> <span class='currency_name'>Paraguayan Guarani</span>" 
                                                 value="PYG">PYG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/QA.png'> <span class='currency_code'>QAR</span> <span class='currency_name'>Qatari Rial</span>" 
                                                 value="QAR">QAR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/RO.png'> <span class='currency_code'>RON</span> <span class='currency_name'>Romanian Leu</span>" 
                                                 value="RON">RON</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/RS.png'> <span class='currency_code'>RSD</span> <span class='currency_name'>Serbian Dinar</span>" 
                                                 value="RSD">RSD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/RU.png'> <span class='currency_code'>RUB</span> <span class='currency_name'>Russian Ruble</span>" 
                                                 value="RUB">RUB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/RW.png'> <span class='currency_code'>RWF</span> <span class='currency_name'>Rwanda Franc</span>" 
                                                 value="RWF">RWF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SA.png'> <span class='currency_code'>SAR</span> <span class='currency_name'>Saudi Riyal</span>" 
                                                 value="SAR">SAR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SB.png'> <span class='currency_code'>SBD</span> <span class='currency_name'>Solomon Islands Dollar</span>" 
                                                 value="SBD">SBD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SC.png'> <span class='currency_code'>SCR</span> <span class='currency_name'>Seychelles Rupee</span>" 
                                                 value="SCR">SCR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SD.png'> <span class='currency_code'>SDG</span> <span class='currency_name'>Sudanese Pound</span>" 
                                                 value="SDG">SDG</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SE.png'> <span class='currency_code'>SEK</span> <span class='currency_name'>Swedish Krona</span>" 
                                                 value="SEK">SEK</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SG.png'> <span class='currency_code'>SGD</span> <span class='currency_name'>Singapore Dollar</span>" 
                                                 value="SGD">SGD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SH.png'> <span class='currency_code'>SHP</span> <span class='currency_name'>Saint Helena Pound</span>" 
                                                 value="SHP">SHP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SL.png'> <span class='currency_code'>SLL</span> <span class='currency_name'>Sierra Leonean Leone</span>" 
                                                 value="SLL">SLL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SO.png'> <span class='currency_code'>SOS</span> <span class='currency_name'>Somali Shilling</span>" 
                                                 value="SOS">SOS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SR.png'> <span class='currency_code'>SRD</span> <span class='currency_name'>Surinam Dollar</span>" 
                                                 value="SRD">SRD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ST.png'> <span class='currency_code'>STD</span> <span class='currency_name'>Sao Tomean Dobra</span>" 
                                                 value="STD">STD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SV.png'> <span class='currency_code'>SVC</span> <span class='currency_name'>El Salvador Colon</span>" 
                                                 value="SVC">SVC</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SY.png'> <span class='currency_code'>SYP</span> <span class='currency_name'>Syrian Pound</span>" 
                                                 value="SYP">SYP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/SZ.png'> <span class='currency_code'>SZL</span> <span class='currency_name'>Swazi Lilangeni</span>" 
                                                 value="SZL">SZL</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TH.png'> <span class='currency_code'>THB</span> <span class='currency_name'>Thai Baht</span>" 
                                                 value="THB">THB</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TJ.png'> <span class='currency_code'>TJS</span> <span class='currency_name'>Tajikistani Somoni</span>" 
                                                 value="TJS">TJS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TM.png'> <span class='currency_code'>TMT</span> <span class='currency_name'>Turkmenistan New Manat</span>" 
                                                 value="TMT">TMT</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TN.png'> <span class='currency_code'>TND</span> <span class='currency_name'>Tunisian Dinar</span>" 
                                                 value="TND">TND</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TO.png'> <span class='currency_code'>TOP</span> <span class='currency_name'>Tongan Pa'anga</span>" 
                                                 value="TOP">TOP</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TR.png'> <span class='currency_code'>TRY</span> <span class='currency_name'>Turkish Lira</span>" 
                                                 value="TRY">TRY</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TT.png'> <span class='currency_code'>TTD</span> <span class='currency_name'>Trinidad and Tobago Dollar</span>" 
                                                 value="TTD">TTD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TW.png'> <span class='currency_code'>TWD</span> <span class='currency_name'>New Taiwan Dollar</span>" 
                                                 value="TWD">TWD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/TZ.png'> <span class='currency_code'>TZS</span> <span class='currency_name'>Tanzanian Shilling</span>" 
                                                 value="TZS">TZS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/UA.png'> <span class='currency_code'>UAH</span> <span class='currency_name'>Ukrainian Hryvnia</span>" 
                                                 value="UAH">UAH</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/UG.png'> <span class='currency_code'>UGX</span> <span class='currency_name'>Uganda Shilling</span>" 
                                                 value="UGX">UGX</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/US.png'> <span class='currency_code'>USD</span> <span class='currency_name'>United States Dollar</span>" 
                                                 value="USD">USD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/UY.png'> <span class='currency_code'>UYU</span> <span class='currency_name'>Peso Uruguayo</span>" 
                                                 value="UYU">UYU</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/UZ.png'> <span class='currency_code'>UZS</span> <span class='currency_name'>Uzbekistan Sum</span>" 
                                                 value="UZS">UZS</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/VE.png'> <span class='currency_code'>VEF</span> <span class='currency_name'>Venezuelan Bolivar</span>" 
                                                 value="VEF">VEF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/VN.png'> <span class='currency_code'>VND</span> <span class='currency_name'>Vietnamese Dong</span>" 
                                                 value="VND">VND</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/VU.png'> <span class='currency_code'>VUV</span> <span class='currency_name'>Vanuatu Vatu</span>" 
                                                 value="VUV">VUV</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/WS.png'> <span class='currency_code'>WST</span> <span class='currency_name'>Samoan Tala</span>" 
                                                 value="WST">WST</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/CF.png'> <span class='currency_code'>XAF</span> <span class='currency_name'>CFA Franc BEAC</span>" 
                                                 value="XAF">XAF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/_unknown.png'> <span class='currency_code'>XCD</span> <span class='currency_name'>East Caribbean Dollar</span>" 
                                                 value="XCD">XCD</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/_unknown.png'> <span class='currency_code'>XOF</span> <span class='currency_name'>CFA Franc BCEAO</span>" 
                                                 value="XOF">XOF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/_unknown.png'> <span class='currency_code'>XPF</span> <span class='currency_name'>CFP Franc</span>" 
                                                 value="XPF">XPF</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/YE.png'> <span class='currency_code'>YER</span> <span class='currency_name'>Yemeni Rial</span>" 
                                                 value="YER">YER</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ZA.png'> <span class='currency_code'>ZAR</span> <span class='currency_name'>South African Rand</span>" 
                                                 value="ZAR">ZAR</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ZM.png'> <span class='currency_code'>ZMW</span> <span class='currency_name'>Zambian Kwacha</span>" 
                                                 value="ZMW">ZMW</option>
                                                                                                        <option data-content="<img class='flag' src='/img/flags/ZW.png'> <span class='currency_code'>ZWL</span> <span class='currency_name'>Zimbabwean Dollar</span>" 
                                                 value="ZWL">ZWL</option>
                                                                                                </select>
                                    </div>
                                </div>	

                                <div class="col-12 text-center py-4" v-if="checkValue">
                                    <span class="font-weight-bold h6">{{ amount }} {{ reversedAmount }} {{ fromCurrencyName }}</span> equals <span class="font-weight-bold h6">{{ result }} {{ toCurrencyName }}</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
</template>

<script>
export default {
    data() {
        return {
            amount: "", 
            reversedAmount: "",
            fromCurrency: "", 
            toCurrency: "",
            result: "",
            getCurr: "",
            fromCurrencyName: "",
            toCurrencyName: "",
            checkValue: false,
            valeu: "",
            currencies: "",
        }
    },
    methods: {
          async getCurrencyNames() {
            if(!!this.amount || !!this.reversedAmount || !!this.fromCurrency && !!this.toCurrency && this.fromCurrency != this.toCurrency){
                let apiKey = '33b45b0c0704d28fa148';
                this.currencies = await this.$axios.get('https://free.currconv.com/api/v7/currencies?apiKey=' + apiKey)
                
                if(!!this.amount && !!this.fromCurrency && !!this.toCurrency && this.fromCurrency != this.toCurrency){
                let value = Object.values(this.currencies.data.results);
            this.getCurr = value.map((i) => { 
                    if(this.fromCurrency == i.id){
                        this.fromCurrencyName = i.currencyName;
                    } else if(this.toCurrency == i.id){
                        this.toCurrencyName = i.currencyName;
                    } else {
                        console.log("error getting currency name")
                    }
                })
                }
                
                if(!!this.reversedAmount && !!this.fromCurrency && !!this.toCurrency && this.fromCurrency != this.toCurrency){
                let value = Object.values(this.currencies.data.results);
            this.getCurr = value.map((i) => { 
                    if(this.toCurrency == i.id){
                        this.fromCurrencyName = i.currencyName;
                    } else if(this.fromCurrency == i.id){
                        this.toCurrencyName = i.currencyName;
                    } else {
                        console.log("error getting the currency names")
                    }
                })
                }
            }else {
                console.log("Unable to convert currency at the moment...")
            }
    },

    async convertCurrency() {
        if(!!this.amount && !!this.fromCurrency && !!this.toCurrency && this.fromCurrency != this.toCurrency){
            this.reversedAmount = "";
        let apiKey = '33b45b0c0704d28fa148';
        let query = this.fromCurrency + '_' + this.toCurrency;

            await this.$axios.get('https://free.currconv.com/api/v7/convert?q=' + query + '&compact=ultra&apiKey=' + apiKey).then(
            (response) => {
                    let val = Object.values(response.data);
                    let total = val * this.amount;
                    this.result = Math.round(total * 100) / 100;

            }).then(this.checkValue = true)

        }else {
                console.log("Unable to convert currency at the moment...")
                }
        },

    async convertCurrencyBackward() {
       if(!!this.reversedAmount && !!this.fromCurrency && !!this.toCurrency && this.fromCurrency != this.toCurrency){
           this.amount = "";
           let apiKey = '33b45b0c0704d28fa148';
           let query = this.toCurrency + '_' + this.fromCurrency;
           
   await this.$axios.get('https://free.currconv.com/api/v7/convert?q=' + query + '&compact=ultra&apiKey=' + apiKey).then(
      (response) => {
            let val = Object.values(response.data);
            let total = val * this.reversedAmount;
            this.result = Math.round(total * 100) / 100;

      }).then(this.checkValue = true)

    }else {
            alert("Unable to convert currency at the moment...")
            }
    }
    
    }
}
</script>
