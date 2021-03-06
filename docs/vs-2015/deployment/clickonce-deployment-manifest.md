---
title: ClickOnce 部署資訊清單 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce, deployment manifests
- deployment manifests [ClickOnce]
ms.assetid: 8457e615-e3b6-4990-8dcf-11bc590e4e9b
caps.latest.revision: 25
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a5d1fe2191dadd0972dcde6f38b9697e29f05ab8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58944331"
---
# <a name="clickonce-deployment-manifest"></a>ClickOnce 部署資訊清單
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

部署資訊清單是 XML 檔案，描述 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 部署，包括要部署的目前 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 應用程式版本之識別。  
  
 部署資訊清單具有下列項目和屬性。  
  
|項目|描述|屬性|  
|-------------|-----------------|----------------|  
|[\<assembly> 元素](../deployment/assembly-element-clickonce-deployment.md)|必要項。 最上層項目。|`manifestVersion`|  
|[\<assemblyIdentity> 元素](../deployment/assemblyidentity-element-clickonce-deployment.md)|必要項。 識別此 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 應用程式的應用程式資訊清單。|`name`<br /><br /> `version`<br /><br /> `publicKeyToken`<br /><br /> `processorArchitecture`<br /><br /> `culture`|  
|[\<description> 元素](../deployment/description-element-clickonce-deployment.md)|必要項。 識別應用程式資訊，這些資訊用於建立殼層的存在和 [控制台] 中的 [新增或移除程式] 項目。|`publisher`<br /><br /> `product`<br /><br /> `supportUrl`|  
|[\<deployment> 元素](../deployment/deployment-element-clickonce-deployment.md)|選擇性。 識別用於更新部署及公開至系統的屬性。|`install`<br /><br /> `minimumRequiredVersion`<br /><br /> `mapFileExtensions`<br /><br /> `disallowUrlActivation`<br /><br /> `trustUrlParameters`|  
|[\<compatibleFrameworks> 元素](../deployment/compatibleframeworks-element-clickonce-deployment.md)|必要項。 識別安裝及執行此應用程式所需的 .NET Framework 版本。|`SupportUrl`|  
|[\<dependency> 元素](../deployment/dependency-element-clickonce-deployment.md)|必要項。 識別部署所要安裝的應用程式版本，以及應用程式資訊清單的位置。|`preRequisite`<br /><br /> `visible`<br /><br /> `dependencyType`<br /><br /> `codebase`<br /><br /> `size`|  
|[\<publisherIdentity> 元素](../deployment/publisheridentity-element-clickonce-deployment.md)|簽署資訊清單的必要項。 包含簽署此部署資訊清單之發行者的資訊。|`Name`<br /><br /> `issuerKeyHash`|  
|[\<Signature> 元素](../deployment/signature-element-clickonce-deployment.md)|選擇性。 包含對此部署資訊清單進行數位簽章時所需的資訊。|None|  
|[\<customErrorReporting> 元素](../deployment/customerrorreporting-element-clickonce-deployment.md)|選擇性。 指定要在錯誤發生時顯示的 URI。|URI|  
  
## <a name="remarks"></a>備註  
 部署資訊清單檔會識別 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 應用程式部署，包含目前的版本與其他部署設定。 這會參考應用程式資訊清單，其中描述此應用程式的目前版本和部署內包含的所有檔案。  
  
 如需詳細資訊，請參閱 [ClickOnce Security and Deployment](../deployment/clickonce-security-and-deployment.md)。  
  
## <a name="file-location"></a>檔案位置  
 部署資訊清單檔案會參考目前應用程式版本的正確應用程式資訊清單。 當您提供新版本的應用程式部署時，必須更新部署資訊清單才能參考新的應用程式資訊清單。  
  
 部署資訊清單檔必須以強式名稱的方式命名，同時也可以包含發行者驗證的憑證。  
  
## <a name="file-name-syntax"></a>檔名語法  
 部署資訊清單的檔名必須以 .application 副檔名做為結尾。  
  
## <a name="examples"></a>範例  
 下列程式碼範例會說明部署資訊清單。  
  
```  
<?xml version="1.0" encoding="utf-8"?>  
<asmv1:assembly xsi:schemaLocation="urn:schemas-microsoft-com:asm.v1 assembly.adaptive.xsd"  
  manifestVersion="1.0"  
  xmlns:asmv3="urn:schemas-microsoft-com:asm.v3"  
  xmlns:dsig=http://www.w3.org/2000/09/xmldsig#  
  xmlns:co.v1="urn:schemas-microsoft-com:clickonce.v1"  
  xmlns:co.v2="urn:schemas-microsoft-com:clickonce.v2"  
  xmlns="urn:schemas-microsoft-com:asm.v2"  
  xmlns:asmv1="urn:schemas-microsoft-com:asm.v1"  
  xmlns:asmv2="urn:schemas-microsoft-com:asm.v2"  
  xmlns:xrml="urn:mpeg:mpeg21:2003:01-REL-R-NS"  
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">  
  <assemblyIdentity   
    name="My Application Deployment.app"  
    version="1.0.0.0"  
    publicKeyToken="43cb1e8e7a352766"  
    language="neutral"  
    processorArchitecture="x86"  
    xmlns="urn:schemas-microsoft-com:asm.v1" />  
  <description  
    asmv2:publisher="My Company Name"  
    asmv2:product="My Application"  
    xmlns="urn:schemas-microsoft-com:asm.v1" />  
  <deployment install="true">  
    <subscription>  
      <update>  
        <expiration maximumAge="0" unit="days" />  
      </update>  
    </subscription>  
    <deploymentProvider codebase="\\myServer\sampleDeployment\MyApplicationDeployment.application" />  
  </deployment>  
  <compatibleFrameworks xmlns="urn:schemas-microsoft-com:clickonce.v2">  
    <framework targetVersion="4.0" profile="Full" supportedRuntime="4.0.20506" />  
    <framework targetVersion="4.0" profile="Client" supportedRuntime="4.0.20506" />  
  </compatibleFrameworks>  
  <dependency>  
    <dependentAssembly  
      dependencyType="install"  
      codebase="1.0.0.0\My Application Deployment.exe.manifest"  
      size="6756">  
      <assemblyIdentity  
        name="My Application Deployment.exe"  
        version="1.0.0.0"  
        publicKeyToken="43cb1e8e7a352766"  
        language="neutral"  
        processorArchitecture="x86"  
        type="win32" />  
      <hash>  
        <dsig:Transforms>  
          <dsig:Transform Algorithm="urn:schemas-microsoft-com:HashTransforms.Identity" />  
        </dsig:Transforms>  
        <dsig:DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />  
        <dsig:DigestValue>E506x9FwNauks7UjQywmzgtd3FE=</dsig:DigestValue>  
      </hash>  
    </dependentAssembly>  
  </dependency>  
<publisherIdentity name="CN=DOMAIN\MyUsername" issuerKeyHash="18312a18a21b215ecf4cdb20f5a0e0b0dd263c08" /><Signature Id="StrongNameSignature" xmlns="http://www.w3.org/2000/09/xmldsig#">  
…  
</Signature></asmv1:assembly>  
```  
  
## <a name="see-also"></a>另請參閱  
 [發行 ClickOnce 應用程式](../deployment/publishing-clickonce-applications.md)
