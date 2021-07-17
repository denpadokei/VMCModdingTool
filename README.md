# VMCModdingTool
VMCのModを作成するときのテンプレートです。  
今のところVS2019に対応してます。

できたcsprjの`VMCDirPath`にVMCのディレクトリパスをコピペなりなんなりすれば動くんじゃないんですかね。



``` xml

<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">

  <PropertyGroup>
    <TargetFramework>net48</TargetFramework>
    <UseWPF>true</UseWPF>
    <VMCDirPath>ここにVMCのディレクトリを入れること。（末尾に\を入れとかないと痛い目を見るので絶対入れましょう。）</VMCDirPath>
  </PropertyGroup>

  <ItemGroup>
    <Reference Include="Assembly-CSharp">
      <Private>false</Private>
      <HintPath>$(VMCDirPath)VirtualMotionCapture_Data\Managed\Assembly-CSharp.dll</HintPath>
    </Reference>
    <Reference Include="com.unity.multiplayer-hlapi.Runtime">
      <Private>false</Private>
      <HintPath>$(VMCDirPath)VirtualMotionCapture_Data\Managed\com.unity.multiplayer-hlapi.Runtime.dll</HintPath>
    </Reference>
    .
    .
    .
</Project>
```
