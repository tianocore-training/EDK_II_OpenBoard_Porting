---?image=assets/images/gitpitch-audience.jpg
@title[EDK_II_OpenBoard_Platform_Porting_pres]
<br><br><br>
<br><br>
## <span class="gold"   >UEFI & EDK II Training</span>
<span style="font-size:0.85em" >EDK II Open Board Platform Design for Intel Architecture(IA)


<br>
<span style="font-size:0.75em" ><a href='http://www.tianocore.org'>tianocore.org</a></span>
Note:
  PITCHME.md for UEFI / EDK II Training  EDK II OpenBoard Platform and Porting  

  Copyright (c) 2019, Intel Corporation. All rights reserved.<BR>

  Redistribution and use in source (original document form) and 'compiled'
  forms (converted to PDF, epub, HTML and other formats) with or without
  modification, are permitted provided that the following conditions are met:

  1) Redistributions of source code (original document form) must retain the
     above copyright notice, this list of conditions and the following
     disclaimer as the first lines of this file unmodified.

  2) Redistributions in compiled form (transformed to other DTDs, converted to
     PDF, epub, HTML and other formats) must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

  THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
  EVENT SHALL TIANOCORE PROJECT  BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
  PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
  OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
  WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
  OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF
  ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.



---  
@title[Lesson Objective]
<BR>
### <p align="center"<span class="gold"   >Lesson Objective </span></p><br>

<!---  Add bullets using https://fontawesome.com/cheatsheet certificate
-->
<ul style="list-style-type:none">
 <li>@fa[certificate gp-bullet-yellow]<span style="font-size:0.9em">&nbsp;&nbsp;Define the porting task list for porting existing <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;open platforms in EDK II</span> </li>
 <li>@fa[certificate gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Determine the necessary porting for each stage <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&amp; boot phase of a new EDK II open platform project </span></li>
</ul>

---?image=/assets/images/slides/Slide3.JPG
@title[Porting Approach]
### <p align="center"><font color="yellow"><b>Approach – Porting EDK II</b></font></p>


@snap[west span-90 fragment]
<br>
<br>
<br>
<br>
@box[bg-royal text-white my-box-pad2  ](<p style="line-height:40%"><span style="font-size:01.1em" ><b>Find Similar Open Board Projects</b><br>&nbsp;</span></p>)
@snapend


@snap[south-east span-85 fragment]
@box[bg-purple-pp text-white my-box-pad2  ](<p style="line-height:40%"><span style="font-size:01.1em" > <b>Staged Approach by Features</b><br>&nbsp;</span></p>)
<br>
@snapend

Note:

- Many examples of packages in the UDK / EDK II source base 
- Find a similar package or platform or Open Board project that meets target project needs
-  Build description files are text files using basic text editor to update – no GUI with the goal of booting to the UEFI Shell


<!---  Section for Porting Task  -->

---?image=assets/images/binary-strings-black2.jpg
<!-- .slide: data-transition="none" -->
@title[Porting Task List Section]
<p align="center"><span style="font-size:01.25em"><font color="#e49436"><b>Porting Task List</b></span></p>

@snap[north-east span-95 ]
<br>
<br>
<br>
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%" ><span style="font-size:0.9em; font-weight: bold;" > <br><br> <br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

<!---  col of numbers Gray -->

@snap[north-west span-10 ]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>&#10102;<br><br><br>&#10103;<br><br><br>&#10104;<br><br><br>&#10105;<br><br><br>&#10106;</font></span></p>
@snapend

<!---  
1
-->


@snap[north-west span-10 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>@color[yellow](&#10102;)<br><br><br>&#10103;<br><br><br>&#10104;<br><br><br>&#10105;<br><br><br>&#10106;</font></span></p>
@snapend



@snap[north-east span-92 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.85em" >
<br>&nbsp;        @color[white](Get the EDK II packages to a local workspace)
<br><br><br>&nbsp;
<br><br><br>&nbsp;
<br><br><br>&nbsp;
<br><br><br>&nbsp;
<br><br>&nbsp;<br><br>&nbsp;  </font></span></p>
@snapend


<!---  
2
-->


@snap[north-west span-10 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>@color[yellow](&#10102;)<br><br><br>@color[yellow](&#10103;)<br><br><br>&#10104;<br><br><br>&#10105;<br><br><br>&#10106;</font></span></p>
@snapend


@snap[north-east span-92 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.85em" >
<br>&nbsp;        @color[white](Get the EDK II packages to a local workspace)
<br><br><br>&nbsp;@color[white](Select the Ref and correct Intel® FSP Package)
<br><br><br>&nbsp;
<br><br><br>&nbsp;
<br><br><br>&nbsp;
<br><br>&nbsp;<br><br>&nbsp;  </font></span></p>@snapend

<!---  
3
-->

@snap[north-west span-10 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>@color[yellow](&#10102;)<br><br><br>@color[yellow](&#10103;)<br><br><br>@color[yellow](&#10104;)<br><br><br>&#10105;<br><br><br>&#10106;</font></span></p>
@snapend


@snap[north-east span-92 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.85em" >
<br>&nbsp;        @color[white](Get the EDK II packages to a local workspace)
<br><br><br>&nbsp;@color[white](Select the Ref and correct Intel® FSP Package)
<br><br><br>&nbsp;@color[white](Copy a reference <font face="Consolas">OpenBoardPkg/BoardXxx</font> )
<br><br><br>&nbsp;
<br><br><br>&nbsp;
<br><br>&nbsp;<br><br>&nbsp;  </font></span></p>
@snapend


<!---  
4
-->

@snap[north-west span-10 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>@color[yellow](&#10102;)<br><br><br>@color[yellow](&#10103;)<br><br><br>@color[yellow](&#10104;)<br><br><br>@color[yellow](&#10105;)<br><br><br>&#10106;</font></span></p>
@snapend


@snap[north-east span-92 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.85em" >
<br>&nbsp;        @color[white](Get the EDK II packages to a local workspace)
<br><br><br>&nbsp;@color[white](Select the Ref and correct Intel® FSP Package)
<br><br><br>&nbsp;@color[white](Copy a reference <font face="Consolas">OpenBoardPkg/BoardXxx</font> )
<br><br><br>&nbsp;@color[white](Use feature stages to port all required project  modules )
<br><br><br>&nbsp;
<br><br>&nbsp;<br><br>&nbsp;  </font></span></p>
@snapend

<!---  
5
-->

@snap[north-west span-10 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>@color[yellow](&#10102;)<br><br><br>@color[yellow](&#10103;)<br><br><br>@color[yellow](&#10104;)<br><br><br>@color[yellow](&#10105;)<br><br><br>@color[yellow](&#10106;)</font></span></p>
@snapend

@snap[north-east span-92 fragment]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.85em" >
<br>&nbsp;        @color[white](Get the EDK II packages to a local workspace)
<br><br><br>&nbsp;@color[white](Select the Ref and correct Intel® FSP Package)
<br><br><br>&nbsp;@color[white](Copy a reference <font face="Consolas">OpenBoardPkg/BoardXxx</font> )
<br><br><br>&nbsp;@color[white](Use feature stages to port all required project  modules )
<br><br><br>&nbsp;@color[white](Validate each stage test points defined w/ each stage)
<br><br>&nbsp;<br><br>&nbsp;  </font></span></p>
@snapend



Note:
4 & 5 take the longest


Find a similar package or platform from the Open Board edk-platforms  that meets target project needs


1. Get the EDK II packages to a local workspace
2. Select the Ref and correct Intel® FSP Package
3. Copy a reference OpenBoardPkg/BoardXXX 
4. Use feature stages to port all required project  modules
5. Validate each stage test point results defined with each stage 



<!---  Section for Porting Task  -->

---?image=assets/images/binary-strings-black2.jpg
<!-- .slide: data-transition="none" -->
@title[Porting Task List Section]
<p align="center"><span style="font-size:01.25em"><font color="#e49436"><b>Porting Task List</b></span></p>

@snap[north-east span-95 ]
<br>
<br>
<br>
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%" ><span style="font-size:0.9em; font-weight: bold;" > <br><br> <br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

<!---  col of numbers Gray -->

@snap[north-west span-10 ]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>&#10102;<br><br><br>&#10103;<br><br><br>&#10104;<br><br><br>&#10105;<br><br><br>&#10106;</font></span></p>
@snapend


@snap[north-west span-10 ]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>@color[yellow](&#10102;)<br><br><br>@color[yellow](&#10103;)<br><br><br>@color[yellow](&#10104;)<br><br><br>&#10105;<br><br><br>&#10106;</font></span></p>
@snapend

@snap[north-east span-92 ]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.85em" >
<br>&nbsp;        @color[yellow](<b>Get the EDK II packages to a local workspace</b>)
<br><br><br>&nbsp;@color[yellow](<b>Select the Ref and correct Intel® FSP Package</b>)
<br><br><br>&nbsp;@color[yellow](<b>Copy a reference <font face="Consolas">OpenBoardPkg/BoardXxx</font></b> )
<br><br><br>&nbsp;@color[#808080](Use feature stages to port all required project  modules )
<br><br><br>&nbsp;@color[#808080](Validate each stage test points defined w/ each stage)
<br><br>&nbsp;<br><br>&nbsp;  </font></span></p>
@snapend



Note:
4 & 5 take the longest


Find a similar package or platform from the Open Board edk-platforms  that meets target project needs


1. Get the EDK II packages to a local workspace
2. Select the Ref and correct Intel® FSP Package
3. Copy a reference OpenBoardPkg/BoardXxx 
4. Use feature stages to port all required project  modules
5. Validate each stage test point results defined with each stage 


---?image=assets/images/slides/Slide6.JPG
@title[Analysis OpenBoard Reference Platforms]
<p align="right"><span class="gold" >@size[1.1em](<b>Analysis OpenBoard Reference Platforms</b>)</span><span style="font-size:0.75em;" ></span></p>
@snap[north-west span-90 ]
<br>
<br>
<span style="font-size:0.8em;" ><br> Steps 1 - 3</span>
<br>
<br>
<ul style="list-style-type:disc; line-height:0.9;">
  <li class=fragment><span style="font-size:0.8em" >Find a similar OpenBoard EDK II Platform in Github <font face="Consolas">edk2_platforms</font> </span> </li>
  <li class=fragment><span style="font-size:0.8em" >Get the reference OpenBoard EDK II Platform from Github </span> </li>
  <li class=fragment><span style="font-size:0.8em" >Build the chosen reference OpenBoard EDK II Platform </span> </li>
  <li class=fragment><span style="font-size:0.8em" >Study the Build directory of the reference OpenBoard </span> </li>
  <li class=fragment><span style="font-size:0.8em" >Study the reference OpenBoard .FDF and .DSC files </span> </li>
  <li class=fragment><span style="font-size:0.8em" >Copy a reference <font face="Consolas">OpenBoardPkg/BoardXxx</font>  to a new name (@size[.8em](i.e <font face="Consolas">NewOpenBoardPkg/NewBoardX</font> where string "@color[#A8ff60](<font face="Consolas">New</font>)" is meaningful to the project.)) </span> </li>
</ul>
@snapend


Note:
https://classroomaid.files.wordpress.com/2012/05/case-study.jpg

This is for steps 1 - 3

---
@title[Get the Reference OpenBoard Source ]
<p align="right"><span class="gold" >@size[1.1em](<b>Get the Reference OpenBoard Source</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<br>
<br>
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-west span-100 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.8em;">
Follow the Build and Download instructions for building the reference open board<br><br>
Download below repository to this WORKSPACE:
</span></p>
@snapend

@snap[north-east span-98 ]
<br>
<br>
<br>
<br>
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
<font face="Arial">edk2 repository and Openssl</font><br>
git clone –recursive https://github.com/tianocore/edk2.git<br>
<br>
<font face="Arial">edk2-platforms repository</font><br>
git clone https://github.com/tianocore/edk2-platforms.git<br>
<br>
<font face="Arial">edk2-non-osi repository</font><br>
git clone https://github.com/tianocore/edk2-non-osi.git -b devel-MinPlatform<br>
<br>
<font face="Arial">FSP repository</font><br>
git clone https://github.com/IntelFsp/FSP.git<br>
</span></p>
@snapend

Note:

Get the source from the open source repositories to a local workspace directory


---
@title[Build the Reference OpenBoard ]
<p align="right"><span class="gold" >@size[1.1em](<b>Build the Reference OpenBoard </b>)</span><span style="font-size:0.75em;" ></span></p>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.8em;">
Open a Command Window and CD to the workspace directory<br><br>
For Linux  - CD  to the edk2 to run the "<font face="Consolas">edksetup.sh</font>" script
</span></p>

```
     $> cd edk2
     $> source edksetup.sh
     $> cd ../
```
<p style="line-height:70%" align="left" ><span style="font-size:0.8em;">
CD  to the Intel directory in edk2-platforms 
</span></p>

```
	$> cd edk2-platforms/Platform/Intel

```

<p style="line-height:70%" align="left" ><span style="font-size:0.8em;">
Run the python build script with the OpenBoard Name (Kabylake is used)
</span></p>

```
    $> python build_bios.py –p KabyLakeRvp3

```


Note:

---
@title[Use the "Build" Directory as a Reference ]
<p align="right"><span class="gold" >@size[1.1em](<b>Use the "Build" Directory as a Reference</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<br>
<br>
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-west span-100 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.8em;">
After the Build is completed the Build directory will be a mirror of all the sources used to build the reference OpenBoard.<br><br>
This can serve as a cross reference to determine what sources are used in the chosen reference OpenBoard.
</span></p>
@snapend

@snap[north-east span-98 ]
<br>
<br>
<br>
<br>
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
&lt;workspace&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;
  Build /KabylakeOpenBoardPkg /KabylakeRvp3 /DEBUG_&lt;BuildTag&gt; /<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    FV /<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    IA32 /<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      &lt;Dirs built for SEC and PEI&gt; /<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    X64 /<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	  &lt;Dirs built for DXE – BDS – Boot&gt; / <br>&nbsp;&nbsp;
</span></p>
@snapend

Note:

---
@title[Study the OpenBoard .DSC and .FDF ]
<p align="right"><span class="gold" >@size[1.1em](<b>Study the OpenBoard .DSC and .FDF</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<p style="line-height:85%" align="left" ><span style="font-size:0.9em;">
Porting requires becoming familiar with the chosen reference platforms DSC and FDF files. 
</span></p>
@snapend

@snap[north-west span-45 fragment ]
<br>
<br>
<br>
<br>
<br>
<br>
@box[bg-royal text-white waved my-box-pad2 ](<p style="line-height:70%" align="center"><span style="font-size:0.75em;" >@size[1.3em](DSC)<br><br>DSC will point to the correct Libraries used in the reference platform<br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-45 fragment ]
<br>
<br>
<br>
<br>
<br>
<br>
@box[bg-royal text-white waved my-box-pad2  ](<p style="line-height:70%" align="center"><span style="font-size:0.75em;" >@size[1.3em](FDF)<br><br>FDF will describe the Flash layout and FVs used for the different stages of the boot<br> flow<br>&nbsp;</span></p>)
@snapend

Note:
To do the porting of the OpenBoard platform requires becoming familiar with the ref openboard platform’s .DSC and FDF files.

FDF will describe the Flash layout and FVs used for the different stages of the boot flow

DSC will point to the correct Libraries used in the reference platform

---
@title[DSC Files for KabyLakeRvp3 ]
<p align="right"><span class="gold" >@size[1.1em](<b>DSC Files for KabyLakeRvp3</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-east span-49 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-west span-49 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
/edk2-platforms/Platform/ <br>&nbsp;&nbsp;
  Intel/KabylakeOpenBoardPkg/<br>&nbsp;&nbsp;&nbsp;&nbsp;
   KabylakeRvp3/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     @color[yellow](OpenBoardPkg.dsc)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     OpenBoardPkgConfig.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     OpenBoardPkgPcd.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     OpenBoardPkgBuildOption.dsc <br><br>
/edk2-platforms/Platform/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
  Intel/MinPlatformPkg/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    Include/Dsc/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      CoreCommonLib.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      CorePeiLib.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      CoreDxeLib.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      CorePeiInclude.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      CoreDxeInclude.dsc<br>&nbsp;&nbsp;
</span></p>
@snapend


@snap[north-east span-45 ]
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
/edk2-platforms/Silicon/ <br>&nbsp;&nbsp;
  Intel/KabylakeSiliconPkg/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiPkgCommonLib.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiPkgPeiLib.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiPkgDxeLib.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiPkgPei.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiPkgDxe.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiPkgBuildOption.dsc
<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[south-east span-45 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; "><br>
<font face="Consolas">@color[yellow](OpenBoardPkg.dsc)</font> – Includes all of the platform, common core,  and silicon related .dsc files
</span></p>
<br>
<br>
@snapend

Note:


By searching the top level include from /edk2-platforms/Platform \ 
<pre>
  Intel/KabylakeOpenBoardPkg \
   KabylakeRvp3
    OpenBoardPkg.dsc
</pre>

We see that it will INCLUDE the other core and silicon .dsc files.  Note the order is important with studying the .DSC files making note of the Sections that the files get included into. 



---
@title[Example: DSC File]
<p align="right"><span class="gold" >@size[1.1em](<b>Example: DSC File</b>)</span><span style="font-size:0.8em;" ></span></p>

```
[Defines]
  #
  # Set platform specific package/folder name, same as passed from PREBUILD script.
  # PLATFORM_PACKAGE would be the same as PLATFORM_NAME as well as package build folder
  # DEFINE only takes effect at R9 DSC and FDF.
  #
  DEFINE      PLATFORM_PACKAGE                = MinPlatformPkg
  DEFINE      PLATFORM_SI_PACKAGE             = KabylakeSiliconPkg
  DEFINE      PLATFORM_SI_BIN_PACKAGE         = KabylakeSiliconBinPkg
  DEFINE      PLATFORM_FSP_BIN_PACKAGE        = AmberLakeFspBinPkg
  DEFINE      PLATFORM_BOARD_PACKAGE          = KabylakeOpenBoardPkg
  DEFINE      BOARD                           = KabylakeRvp3
  DEFINE      PROJECT                         = $(PLATFORM_BOARD_PACKAGE)/$(BOARD)

  #
  # Platform On/Off features are defined here
  #
  !include OpenBoardPkgConfig.dsc
  !include OpenBoardPkgPcd.dsc

[Defines]
!if gIntelFsp2WrapperTokenSpaceGuid.PcdFspModeSelection == 1
  #
  # For backward compatibility API mode will use KabylakeFspBinPkg.
  # KabylakeFspBinPkg only supports API mode.
  #
  DEFINE      PLATFORM_FSP_BIN_PACKAGE        = KabylakeFspBinPkg
!else
  #
  # AmberLakeFspBinPkg supports both API and Dispatch modes
  #
  DEFINE      PLATFORM_FSP_BIN_PACKAGE        = AmberLakeFspBinPkg
!endif

################################################################################
#
# Defines Section - statements that will be processed to create a Makefile.
#
################################################################################
[Defines]
  PLATFORM_NAME                       = $(PLATFORM_PACKAGE)
  PLATFORM_GUID                       = 465B0A0B-7AC1-443b-8F67-7B8DEC145F90
  PLATFORM_VERSION                    = 0.1
  DSC_SPECIFICATION                   = 0x00010005
  OUTPUT_DIRECTORY                    = Build/$(PROJECT)
  SUPPORTED_ARCHITECTURES             = IA32|X64
  BUILD_TARGETS                       = DEBUG|RELEASE
  SKUID_IDENTIFIER                    = ALL


  FLASH_DEFINITION                    = $(PROJECT)/OpenBoardPkg.fdf

  FIX_LOAD_TOP_MEMORY_ADDRESS         = 0x0
  DEFINE   TOP_MEMORY_ADDRESS         = 0x0

  #
  # Default value for OpenBoardPkg.fdf use
  #
  DEFINE BIOS_SIZE_OPTION = SIZE_70

################################################################################
#
# SKU Identification section - list of all SKU IDs supported by this
#                              Platform.
#
################################################################################
[SkuIds]
  0|DEFAULT              # The entry: 0|DEFAULT is reserved and always required.
  4|KabylakeRvp3
  0x60|KabyLakeYLpddr3Rvp3

################################################################################
#
# Library Class section - list of all Library Classes needed by this Platform.
#
################################################################################

!include $(PLATFORM_PACKAGE)/Include/Dsc/CoreCommonLib.dsc
!include $(PLATFORM_PACKAGE)/Include/Dsc/CorePeiLib.dsc
!include $(PLATFORM_PACKAGE)/Include/Dsc/CoreDxeLib.dsc
 . . ..


```


@snap[south-east span-45 ]
<p style="line-height:40% " align="right"><span style="font-size:0.55em;">
Link to <a href="https://github.com/tianocore/edk2-platforms/blob/master/Platform/Intel/KabylakeOpenBoardPkg/KabylakeRvp3/OpenBoardPkg.dsc"> Kabylake .DSC </a>
file
</span></p>
@snapend

Note:

Click on the link to view the whole .DSC file

---
@title[FDF Files for KabyLakeRvp3 ]
<p align="right"><span class="gold" >@size[1.1em](<b>FDF Files for KabyLakeRvp3</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-47 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-52 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
/edk2-platforms/Platform/  <br>&nbsp;&nbsp;
  Intel/KabylakeOpenBoardPkg/<br>&nbsp;&nbsp;&nbsp;&nbsp;
   Include/Fdf/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      FlashMapInclude.fdf<br>&nbsp;&nbsp;&nbsp;&nbsp;
   KabylakeRvp3<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    @color[yellow](OpenBoardPkg.fdf)<br>&nbsp;&nbsp;

<br>&nbsp;&nbsp;
</span></p>
@snapend


@snap[north-east span-50 ]
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
/edk2-platforms/Platform/ <br>&nbsp;&nbsp;
  Intel/MinPlatformPkg/<br>&nbsp;&nbsp;
  Include/Fdf/<br>&nbsp;&nbsp;&nbsp;&nbsp;
     CorePreMemoryInclude.fdf<br>&nbsp;&nbsp;&nbsp;&nbsp;
     CorePostMemoryInclude.fdf<br>&nbsp;&nbsp;&nbsp;&nbsp;
     CoreUefiBootInclude.fdf<br>&nbsp;&nbsp;&nbsp;&nbsp;
     CoreOsBootInclude.fdf<br>&nbsp;&nbsp;&nbsp;&nbsp;
     CoreSecurityPreMemoryInclude.fdf<br>&nbsp;&nbsp;&nbsp;&nbsp;
     CoreSecurityPostMemoryInclude.fdf<br>&nbsp;&nbsp;&nbsp;&nbsp;
     CoreSecurityLateInclude.fdf<br>&nbsp;&nbsp;&nbsp;&nbsp;
     RuleInclude.fdf<br>&nbsp;&nbsp;
<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[south-west span-47 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; "><br>
<font face="Consolas">@color[yellow](OpenBoardPkg.fdf)</font> – Includes all of the platform and common core related .fdf files
</span></p>
<br>
<br>
@snapend

Note:

Similar to the .DSC, by searching the top level include from /edk2-platforms/Platform \ 
<pre>
  Intel/KabylakeOpenBoardPkg \
   KabylakeRvp3
    OpenBoardPkg.fdf
</pre>

We see that it will INCLUDE the other common core  files.  also Note, 
the order is important with studying the .FDF files making note of the Sections that the files get included into. 

This determines where in the flash map FV and Modules will be placed..

---?image=assets/images/slides/Slide14.JPG
@title[Flash Layout for Kabylake ]
<p align="right"><span class="gold" >@size[1.1em](<b>Flash Layout for Kabylake</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
edk2-platforms/Platform/ <br>&nbsp;&nbsp;
  Intel/<br>&nbsp;&nbsp;&nbsp;&nbsp;
   KabylakeOpenBoardPkg/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    Include/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     Fdf/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      @color[yellow](FlashMapInclude.fdf)
<br>&nbsp;&nbsp;
</span></p>
@snapend


Note:

The mapping closely corresponds to the different FV that get created as part of the build process


---
@title[Example: Kabylake  .FDF file ]
<p align="right"><span class="gold" >@size[1.1em](<b>Example: Kabylake .FDF file</b>)</span><span style="font-size:0.8em;" ></span></p>

```
[FD.KabylakeRvp3]
 #
  . . .
[FV.FvPreMemory]
BlockSize          = $(FLASH_BLOCK_SIZE)
FvAlignment        = 16
  . . .
INF  UefiCpuPkg/SecCore/SecCore.inf
INF  MdeModulePkg/Core/Pei/PeiMain.inf
!include $(PLATFORM_PACKAGE)/Include/Fdf/CorePreMemoryInclude.fdf

INF $(PLATFORM_PACKAGE)/PlatformInit/ReportFv/ReportFvPei.inf
INF $(PLATFORM_PACKAGE)/PlatformInit/PlatformInitPei/PlatformInitPreMem.inf
INF IntelFsp2WrapperPkg/FspmWrapperPeim/FspmWrapperPeim.inf
INF $(PLATFORM_PACKAGE)/PlatformInit/SiliconPolicyPei/SiliconPolicyPeiPreMem.inf

. . .

[FV.FvPostMemoryUncompact]
BlockSize          = $(FLASH_BLOCK_SIZE)
FvAlignment        = 16
ERASE_POLARITY     = 1
 . . .

!include $(PLATFORM_PACKAGE)/Include/Fdf/CorePostMemoryInclude.fdf

# Init Board Config PCD
INF $(PLATFORM_PACKAGE)/PlatformInit/PlatformInitPei/PlatformInitPostMem.inf
INF IntelFsp2WrapperPkg/FspsWrapperPeim/FspsWrapperPeim.inf
INF $(PLATFORM_PACKAGE)/PlatformInit/SiliconPolicyPei/SiliconPolicyPeiPostMem.inf

  . . .

[FV.FvUefiBootUncompact]
BlockSize          = $(FLASH_BLOCK_SIZE)
FvAlignment        = 16
 . . .

!include $(PLATFORM_PACKAGE)/Include/Fdf/CoreUefiBootInclude.fdf

INF  UefiCpuPkg/CpuDxe/CpuDxe.inf
INF  MdeModulePkg/Bus/Pci/PciHostBridgeDxe/PciHostBridgeDxe.inf

INF  MdeModulePkg/Bus/Pci/SataControllerDxe/SataControllerDxe.inf
INF  MdeModulePkg/Bus/Ata/AtaBusDxe/AtaBusDxe.inf
INF  MdeModulePkg/Bus/Ata/AtaAtapiPassThru/AtaAtapiPassThru.inf
INF  MdeModulePkg/Universal/Console/GraphicsOutputDxe/GraphicsOutputDxe.inf

INF  ShellPkg/Application/Shell/Shell.inf

INF  $(PLATFORM_PACKAGE)/PlatformInit/PlatformInitDxe/PlatformInitDxe.inf
INF  IntelFsp2WrapperPkg/FspWrapperNotifyDxe/FspWrapperNotifyDxe.inf

INF  $(PLATFORM_PACKAGE)/Test/TestPointStubDxe/TestPointStubDxe.inf



```


@snap[south-east span-45 ]
<p style="line-height:40% " align="right"><span style="font-size:0.55em;">
Link to <a href="https://github.com/tianocore/edk2-platforms/blob/master/Platform/Intel/KabylakeOpenBoardPkg/KabylakeRvp3/OpenBoardPkg.fdf"> Kabylake .FDF </a>
file
</span></p>
@snapend

Note:

Click on the link to view the whole .FDF file


---
@title[Copy a Similar Reference OpenBoard]
<p align="right"><span class="gold" >@size[1.1em](<b>Copy a Similar Reference OpenBoard</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-50 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-98 ]
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
MyWorkSpace/<br>&nbsp;&nbsp;
edk2/<br>&nbsp;&nbsp; &nbsp;&nbsp;
  - "@color[#FFC000](edk2 Common)"<br>&nbsp;&nbsp;
edk2-platforms/<br>&nbsp;&nbsp;&nbsp;&nbsp;
  Platform/ "@color[#FFC000](Platform)"<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     Intel/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       MinPlatformPkg/ "@color[#FFC000](Board common)"<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       KabylakeOpenBoardPkg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       @color[yellow](NewOpenBoardPkg)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
           @color[yellow](BoardXxx)/ "@color[#FFC000](Board)"<br>&nbsp;&nbsp;&nbsp;&nbsp;
  Silicon/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
     Intel/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       KabyLakeSilconPkg/"@color[#FFC000](Silicon)"<br>&nbsp;&nbsp;
edk2-non-osi/<br>&nbsp;&nbsp;&nbsp;&nbsp;
  Silicon/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     Intel/<br>&nbsp;&nbsp;
FSP/"Silicon"<br>&nbsp;&nbsp;&nbsp;&nbsp;
  KabyLakeFspBinPkg<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north span-5 ]
<br>
<br>
<br>
<ul style="list-style-type:none; line-height:0.7;">
  <li><span style="font-size:0.65em" >@color[gray]( 1. )<br><br></span> </li>
  <li><span style="font-size:0.65em" >@color[gray]( 2. )<br><br> </span> </li>
  <li><span style="font-size:0.65em" > 3. </span> </li>
</ul>
@snapend


@snap[north-east span-48 ]
<br>
<br>
<br>
<ul style="list-style-type:none; line-height:0.7;">
  <li><span style="font-size:0.65em" > @color[gray](Get the EDK II packages locally to the workspace)</span> </li>
  <li><span style="font-size:0.65em" > @color[gray](Select the Ref  OpenBoard and correct Intel® FSP silicon initialization solution)</span> </li>
  <li class=fragment><span style="font-size:0.65em" > Copy a reference - <font face="Consolas">GenerationOpenBoardPkg/BoardXxx</font> to a new directory  </span> </li>
</ul>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; "><br>
<font face="Consolas">@color[yellow](NewOpenBoardPkg) & @color[yellow](BoardXxx)</font>
</span></p>
<br>
<br>
@snapend

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Only make changes in the "<font face="Consolas">@color[yellow](NewOpenBoardPkg)</font>"<br><br>&nbsp;</span></p>)
@snapend


Note:


The build process creates this directory - Build/

MyWorkSpace – directory from the “git” of repositories

Build –p .dsc from the BOARD Directory

The architecture is designed to support a maintainer ownership model. For example, board developers should not directly modify (fork) the platform, silicon, or common code. More details on conventional usage of the package classifications can be found in supplemental literature from UEFI Forum, TianoCore.org, and others.
  (see https://github.com/tianocore/tianocore.github.io/wiki/EDK-II-Development-Process)


---
@title[PI Modules – One board, one dir]
<p align="right"><span class="gold" >@size[1.1em](<b>PI Modules – One board, one dir</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-98 ]
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
@color[yellow](KabylakeOpenBoardPkg)<br>&nbsp;&nbsp;
  Acpi<br>&nbsp;&nbsp;
  FspWrapper<br>&nbsp;&nbsp;&nbsp;&nbsp;
    Library<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PeiFspPolicyUpdateLib<br>&nbsp;&nbsp;
  Include<br>&nbsp;&nbsp;
  Library<br>&nbsp;&nbsp;
  @color[yellow](KabylakeRvp3)<br>&nbsp;&nbsp;
   . . .<br>&nbsp;&nbsp;
  @color[yellow](KabylakeRvp7 )<br>&nbsp;&nbsp;&nbsp;&nbsp;
    Include<br>&nbsp;&nbsp;&nbsp;&nbsp;
    Library<br>&nbsp;&nbsp;&nbsp;&nbsp;
       . . .<br>&nbsp;&nbsp;&nbsp;&nbsp;
    OpenBoardPkg.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;
    OpenBoardPkg.fdf
<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-47 ]
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
@color[yellow](KabylakeRvp7 )<br>&nbsp;&nbsp;
  Library<br>&nbsp;&nbsp;&nbsp;&nbsp;
    BoardInitLib<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PeiBoardInitPreMemLib<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PeiBoardInitPostMemLib<br>&nbsp;&nbsp;&nbsp;&nbsp;
<br>&nbsp;&nbsp;<br>&nbsp;&nbsp;&nbsp;&nbsp;
  
    BasePlatformHookLib<br>&nbsp;&nbsp;<br>&nbsp;&nbsp;&nbsp;&nbsp;

    BoardAcpiLib<br>&nbsp;&nbsp;

<br>&nbsp;&nbsp;
</span></p>
@snapend


@snap[north-east span-78 fragment ]
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
 @fa[arrow-left fa-2x gp-bullet-yellow] 
<br>
 @fa[arrow-left fa-2x gp-bullet-yellow] 
</span></p>
@snapend



Note:

This example KabylakeRvp3 and KabylakeRvp7 are very similar but different enough to make a new directory for KabylakeRvp7

If we need to add a new board, such as Rvp7, we can copy the KabylakeRv3 folder to KabylakeRvp7 folder, and update all the modules in this KabylakeRvp7. 
Once we move the board specific code to the board specific directory, the generic board code should not contain any board specific code. For example, we do not put PeiFspPolicyUpdateLib 
into KabylakeRvp3, because this code only consumes a set of PCDs, such as PcdMrcRcompResistor, PcdSpecificLpHsioPtssTable1, PcdHdaVerbTable, etc. A KabylakeRvp3 board specific code BoardInitLib 
produces these PCDs and Kabylake common board code consumes these PCDs 



---
@title[New OpenBoard Directory]
<p align="right"><span class="gold" >@size[1.1em](<b>New OpenBoard Directory</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-98 ]
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
@color[yellow](NwqOpenBoardPkg)<br>&nbsp;&nbsp;
  Acpi<br>&nbsp;&nbsp;
  FspWrapper<br>&nbsp;&nbsp;&nbsp;&nbsp;
    Library<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PeiFspPolicyUpdateLib<br>&nbsp;&nbsp;
  Include<br>&nbsp;&nbsp;
  Library<br>&nbsp;&nbsp;
   @color[yellow](BoardXxx )<br>&nbsp;&nbsp;&nbsp;&nbsp;
    Include<br>&nbsp;&nbsp;&nbsp;&nbsp;
    Library<br>&nbsp;&nbsp;&nbsp;&nbsp;
       . . .<br>&nbsp;&nbsp;&nbsp;&nbsp;
    OpenBoardPkg.dsc<br>&nbsp;&nbsp;&nbsp;&nbsp;
    OpenBoardPkg.fdf
<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-47 ]
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
@color[yellow](BoardXxx )<br>&nbsp;&nbsp;
  Library<br>&nbsp;&nbsp;&nbsp;&nbsp;
    BoardInitLib<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PeiBoardInitPreMemLib<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PeiBoardInitPostMemLib<br>&nbsp;&nbsp;&nbsp;&nbsp;
<br>&nbsp;&nbsp;<br>&nbsp;&nbsp;&nbsp;&nbsp;
  
    BasePlatformHookLib<br>&nbsp;&nbsp;<br>&nbsp;&nbsp;&nbsp;&nbsp;

    BoardAcpiLib<br>&nbsp;&nbsp;

<br>&nbsp;&nbsp;
</span></p>
@snapend



Note:

This example we are coping the KabylakeOpenBoardPkg to the NewOpenBoardPkg since the board had many differences

Example the flash layout is too different to use the same platform common board.

Also rename the board to a meaningful name, this case “BoardXxx”



<!---  Section for Porting Task  -->

---?image=assets/images/binary-strings-black2.jpg
<!-- .slide: data-transition="none" -->
@title[Porting Task List Section]
<p align="center"><span style="font-size:01.25em"><font color="#e49436"><b>Porting Task List</b></span></p>

@snap[north-east span-95 ]
<br>
<br>
<br>
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%" ><span style="font-size:0.9em; font-weight: bold;" > <br><br> <br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

<!---  col of numbers Gray -->

@snap[north-west span-10 ]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>&#10102;<br><br><br>&#10103;<br><br><br>&#10104;<br><br><br>&#10105;<br><br><br>&#10106;</font></span></p>
@snapend


@snap[north-west span-10 ]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:01.0em" ><font color="#808080"><br><br>&#10102;<br><br><br>&#10103;<br><br><br>&#10104;<br><br><br>@color[yellow](&#10105;)<br><br><br>@color[yellow](&#10106;)</font></span></p>
@snapend


@snap[north-east span-92 ]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.85em" >
<br>&nbsp;        @color[#808080](Get the EDK II packages to a local workspace)
<br><br><br>&nbsp;@color[#808080](Select the Ref and correct Intel® FSP Package)
<br><br><br>&nbsp;@color[#808080](Copy a reference <font face="Consolas">OpenBoardPkg/BoardXxx</font>)
<br><br><br>&nbsp;@color[yellow](<b>Use feature stages to port all required project  modules</b> )
<br><br><br>&nbsp;@color[yellow](<b>Validate each stage test points defined w/ each stage</b>)
<br><br>&nbsp;<br><br>&nbsp;  </font></span></p>
@snapend



Note:
4 & 5 take the longest


Find a similar package or platform from the Open Board edk-platforms  that meets target project needs


1. Get the EDK II packages to a local workspace
2. Select the Ref and correct Intel® FSP Package
3. Copy a reference OpenBoardPkg/BoardXxx
4. Use feature stages to port all required project  modules
5. Validate each stage test point results defined with each stage 

---?image=assets/images/binary-strings-black2.jpg
@title[Port by Stages Section 1]
<br><br><br><br><br>
## <span class="gold"  >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Port by Stages</span>
<span style="font-size:0.9em" > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Use the staged architecture as a porting guide</span>


---?image=assets/images/slides/Slide_TableDHote.JPG
@title[Staged Approach by Features Section]
<p align="right"><span class="gold" >@size[1.1em](<b>Staged Approach by Features</b>)</span><br><span style="font-size:0.75em;" >- Platform Firmware Boot Stage PCD</span></p>
@snap[north-west span-70 ]
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.8em;" >PCD Variable:<br></span>
<span style="font-size:0.5em; font-family:Consolas;">
gPlatformModuleTokenSpaceGuid.PcdBootStage
</span></p>
@snapend

@snap[north-west span-50 ]
<br>
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >Stage 1&nbsp;</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >Enable Debug &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >Stage 2&nbsp;</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >Memory Initialization</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >Stage 3&nbsp;</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >Boot to UEFI Shell only &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >Stage 4&nbsp;</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >Boot ot OS</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >Stage 5&nbsp;</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >Boot ot OS w/ Security enabled&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >Stage 6&nbsp;</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >Advanced Feature Selection</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >Stage 7&nbsp;</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >Performance Opetimizations &nbsp;</span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south-east span-45 ]
<p style="line-height:50%" align="left" ><span style="font-size:0.6em;" >
PCD Is tested within .FDF to see which modules to include 
</span></p>
@snapend

Note:
table d’hôte  Pronounced "Tab la dout"
Image source: http://3.bp.blogspot.com/-nCzQh7Xu3_I/Uzk1a4DRk-I/AAAAAAAABCY/lQvT1cbn8Ug/s1600/5892-Caucasian-Man-Sitting-At-A-Table-And-Reading-A-Menu-At-A-Restaurant-Clipart-Illustration.jpg



Depending on the stage # provides some idea regarding what components are needed for a BIOS solution. It can be 3M full featured BIOS, or only 256K if just the basic boot is required, in some cases. 

This work can be done by defining some default configuration in PlatformConfig.dsc. 
For example, PcdBootStage|4 can be used to configure a BIOS to support a boot to OS (with ACPI/SMM), or PcdBootStage|3 to configure a BIOS to boot to shell only (without ACPI/SMM) 

- Stage I - Minimal Debug
  - Serial Port, Port 80, External debuggers Optional: Software debugger
- Stage II  - Memory Functional
  - Basic hardware initialization including main memory
- Stage III - Boot to UEFI Shell
   - Generic DXE driver execution
- Stage IV - Boot to OS
  - Boot a general purpose operating system with the minimally required feature set. Publish a minimal set of ACPI tables. Stage V -Security Enabled
  - UEFI Secure Boot, TCG trusted boot, DMA protection, etc.
- Stage VI - Advanced Feature Selection
  - Firmware update, power management, networking support, manageability, testability, reliability, availability, serviceability, non-essential provisioning and resiliency mechanisms
- Stage VII – Tuning
   - Size and performance optimizations

Within the DSC and  FDF choose which modules to include based on PCD
Example
<pre>
DSC:
[PcdsFeatureFlag]
  gMinPlatformPkgTokenSpaceGuid.PcdStopAfterDebugInit|FALSE
  gMinPlatformPkgTokenSpaceGuid.PcdStopAfterMemInit|FALSE
  gMinPlatformPkgTokenSpaceGuid.PcdBootToShellOnly|FALSE
  gMinPlatformPkgTokenSpaceGuid.PcdUefiSecureBootEnable|FALSE
  gMinPlatformPkgTokenSpaceGuid.PcdTpm2Enable|FALSE

!if gMinPlatformPkgTokenSpaceGuid.PcdBootStage >= 1
 gMinPlatformPkgTokenSpaceGuid.PcdStopAfterDebugInit|TRUE
!endif

Example FDF
!if gMinPlatformPkgTokenSpaceGuid.PcdBootToShellOnly == FALSE
INF  MdeModulePkg/Universal/FaultTolerantWriteDxe/FaultTolerantWriteSmm.inf
INF  MdeModulePkg/Universal/Variable/RuntimeDxe/VariableSmmRuntimeDxe.inf
INF  MdeModulePkg/Universal/Variable/RuntimeDxe/VariableSmm.inf
!endif
</pre>



---?image=assets/images/slides/Slide_TableDHote.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Staged Approach by Features Section 01]
<p align="right"><span class="gold" >@size[1.1em](<b>Staged Approach by Features</b>)</span><br><span style="font-size:0.75em;" >- Platform Firmware Boot Stage PCD</span></p>


@snap[north-west span-50 ]
<br>
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Stage 1&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Enable Debug &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 2&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Memory Initialization)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 3&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot to UEFI Shell only &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 4&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 5&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS w/ Security enabled&nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 6&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Advanced Feature Selection)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 7&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Performance Opetimizations &nbsp;)</span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south-east span-45 ]
<p style="line-height:50%" align="left" ><span style="font-size:0.6em;" >
PCD Is tested within .FDF to see which modules to include 
</span></p>
@snapend



@snap[south-east span-13 ]
<p style="line-height:20%" align="left" ><span style="font-size:02.1em;" >
1
<br><br>
</span></p>
<br><br>
@snapend

Note:
table d’hôte  
Image source: http://3.bp.blogspot.com/-nCzQh7Xu3_I/Uzk1a4DRk-I/AAAAAAAABCY/lQvT1cbn8Ug/s1600/5892-Caucasian-Man-Sitting-At-A-Table-And-Reading-A-Menu-At-A-Restaurant-Clipart-Illustration.jpg



Depending on the stage # provides some idea regarding what components are needed for a BIOS solution. It can be 3M full featured BIOS, or only 256K if just the basic boot is required, in some cases. 

This work can be done by defining some default configuration in PlatformConfig.dsc. 
For example, PcdBootStage|4 can be used to configure a BIOS to support a boot to OS (with ACPI/SMM), or PcdBootStage|3 to configure a BIOS to boot to shell only (without ACPI/SMM) 

- Stage I - Minimal Debug
  - Serial Port, Port 80, External debuggers Optional: Software debugger
- Stage II  - Memory Functional
  - Basic hardware initialization including main memory
- Stage III - Boot to UEFI Shell
   - Generic DXE driver execution
- Stage IV - Boot to OS
  - Boot a general purpose operating system with the minimally required feature set. Publish a minimal set of ACPI tables.- Stage V -Security Enabled
  - UEFI Secure Boot, TCG trusted boot, DMA protection, etc.
- Stage VI - Advanced Feature Selection
  - Firmware update, power management, networking support, manageability, testability, reliability, availability, serviceability, non-essential provisioning and resiliency mechanisms
- Stage VII – Tuning
   - Size and performance optimizations


---?image=assets/images/slides/Slide23.JPG
@title[Boot Flow – Stage 1]
<p align="right"><span class="gold" >@size[1.1em](<b>Boot Flow – Stage 1</b>)</span><span style="font-size:0.75em;" ></span></p>


Note:

Stage I is contained within SEC and PEI phases. Code must not be compressed and content must be capable of being mapped to memory by hardware or other firmware.



---?image=assets/images/slides/Slide24.JPG
@title[High Level Control Flow – Stage 1]
<p align="right"><span class="gold" >@size[1.1em](<b>High Level Control Flow – Stage 1</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-east span-50 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.85em; "><br>
Major Execution Activities
</span></p>

<ul style="list-style-type:disc; line-height:0.8;">
  <li><span style="font-size:0.8em" > Establish temporary memory (initialize MTRR)</span> </li>
  <li><span style="font-size:0.8em" > Perform pre-memory board-specific initialization</span> </li>
  <li><span style="font-size:0.8em" > Board detection</span> </li>
  <li><span style="font-size:0.8em" > GPIOs</span> </li>
  <li><span style="font-size:0.8em" > Serial Port initialization (Example: SIO, HSUART)</span> </li>
</ul>
@snapend

Note:

The objective of Stage I is to provide a foundation for more complex development in later stages. The board should implement a board-specific minimal code path capable of firmware debug output. Basic debug capability serves as a base for development activities in later stages. As Stage I is inherently foundational to product execution it may include more content and complexity than the functionality strictly required for debug output.


These activities, contained within SEC and PEI phases, do not map 1:1 to the required functions. Some of this flow is already well defined by UEFI or EDK II specifications. 


---?image=assets/images/slides/Slide25.JPG
@title[Location of Stage 1 Modules]
<p align="right"><span class="gold" >@size[1.1em](<b> Location of Stage 1 Modules</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Check the Board/Platform .FDF file layout<br><br>&nbsp;</span></p>)
@snapend


Note:

Where’s the platform code start? or the first point where the platform code is executed


As the foundational stage for further functionality, Stage I may include additional content beyond what is strictly required to meet the stage objective. Typically this will include silicon initialization code that may be packaged in a variety of mechanisms including varying size binary blobs. 

The Stage I modules will be combined into FVs to make up the Stage I components

---
@title[Stage 1 Firmware Volumes]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 1 Firmware Volumes</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Name&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Content</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvPreMemory&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >SEC + StatusCode&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvBspPreMemory&nbsp;</span></p></td>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >Pre-memory board initialization</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvFspT&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >SEC silicon initialization - T-RAM &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvFspM&nbsp;</span></p></td>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >Memory initialization</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;-&gt;FvPreMemorySilicon&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >Pre-memory silicon initialization&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvFspS&nbsp;</span></p></td>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >Silicon initialization</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;-&gt;FvPostMemorySilicon&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".0%2"><p style="line-height:01%"><span style="font-size:0.5em" >Post-memory silicon initialization &nbsp;</span></p></td>
	</tr>
</table>
<br>
@snapend



Note:


Use the Platform .Fdf File to determine which modules map to each FV
Typically this will include silicon initialization code that may be packaged in a variety of mechanisms including varying size binary blobs. In the layout shown in this slide, the Intel® FSP solution is shown as an example. In this case, the FSP binary can be rebased and integrated in one step rather than distributing the work for the FSP-M and FSP-S rebase unnecessarily across later stages. 
A Note that a child FV is a FV embedded within the parent FV. The child FV is identified by a file type of EFI_FV_FILETYPE_FIRMWARE_VOLUME_IMAGE.



| `Name`              | `Content`                          | `Compressed` | `Parent FV` |
| ------------------- | ---------------------------------- | ------------ | ----------- |
| FvPreMemory         | SEC + StatusCode                   | No           | None        |
| FvBspPreMemory      | Pre-memory board initialization    | No           | None        |
| FvFspT              | SEC silicon initialization         | No           | None        |
| FvFspM              | Memory initialization              | No           | None        |
| FvPreMemorySilicon  | Pre-memory silicon initialization  | No           | FvFspM      |
| FvFspS              | Silicon initialization             | No           | None        |
| FvPostMemorySilicon | Post-memory silicon initialization | Yes          | FvFspS      |




---
@title[Stage 1 FVs Contents]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 1 FVs Contents</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>FV&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Components</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Purpose</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvPreMemory&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >@color[yellow](SecCore.efi)&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".020%" width="70%"><p style="line-height:022%"><span style="font-size:0.45em" >
			&bull; &nbsp;Reset Vector<br>
			&bull; &nbsp;Passes PEI core the address of FvFspM<br>
			&bull; &nbsp;Passes PEI core the debug configuration
		&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >ReportFvPei.efi&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" >Installs firmware volumes</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >PlatformInitPreMemory.efi&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" >Performs pre memory initialization&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >SiliconPolicyPeiPreMemory.efi&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" >Publishes silicon initialization configuration&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvFspT&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >TempRamInit API &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" >Set up Temp Memory (CAR)&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvFspM&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >FspmWrapperPeim.efi&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" >call FspMemoryInit API&nbsp;</span></p></td>
	</tr>
</table>
<br>
@snapend

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Mapped according to .FDF file layout<br><br>&nbsp;</span></p>)
@snapend


Note:


Use the Platform .Fdf File to determine which modules map to each FV


https://github.com/tianocore-docs/edk2-MinimumPlatformSpecification/blob/master/3_stage_1_minimum_debug/32_firmware_volumes.md#32-firmware-volumes


As the foundational stage for further functionality, Stage I may include additional content beyond what is strictly required to meet the stage objective. Typically this will include silicon initialization code that may be packaged in a variety of mechanisms including varying size binary blobs. In the layout shown in this slide, the Intel® FSP solution is shown as an example. In this case, the FSP binary can be rebased and integrated in one step rather than distributing the work for the FSP-M and FSP-S rebase unnecessarily across later stages. Note that a child FV is a FV embedded within the parent FV. The child FV is identified by a file type of EFI_FV_FILETYPE_FIRMWARE_VOLUME_IMAGE.
| `Binary` | `FV`              | `Components`                  | `Purpose`                                                                                                                      |
| -------- | ----------------- | ----------------------------- | --------------------------------------------------------------------------------------- |
| Stage I  | FvPreMemory.fv    | SecCore.efi                   |  Reset Vector - Passes PEI core the address of FvFspM - Passes PEI core the debug configuration   |
|          |                   | ReportFvPei.efi               |  Installs firmware volumes                                                                                     |
|          |                   | SiliconPolicyPeiPreMemory.efi |  Publishes silicon initialization configuration                                                                |
|          |                   | PlatformInitPreMemory.efi     |  Performs pre memory initialization                                                                            |
|          |                   | Additional Components         |  Additional pre-memory components required for Stage I boot                                                    |
|          | FvBspPreMemory.fv | Additional Components         |  Advanced pre-memory board support components                                                                  |
|          | FvFspT.fv         | PlatformSec.efi               |  Initializes T-RAM silicon functionality                                                                       |
|          |                   |                               |  Tests T-RAM functionality                                                                                     |
|          |                   | Additional Components         |                                                                                                                                |
|          | FvFspM.fv         | PeiCore.efi                   |  PEI services and dispatcher                                                                                   |
|          |                   | PcdPeim.efi                   |  PCD service                                                                                                   |
|          |                   | FspPlatform.efi               |  Converts UPD to Policy PPI                                                                                    |
|          |                   | FvPreMemorySilicon.fv         |                                                                                                                                |
|          |                   | (child FV)                    |                                                                                                                                |
|          |                   | Additional Components         |  Pre-memory silicon initialization components                                                                  |
|          |                   | ReportStatusCodeRouterPei.efi |  Provide status code infrastructure                                                                            |
|          |                   | StatusCodeHandlerPei.efi      |  Provide status code listeners                                                                                 |
|          |                   | Additional Components         |                                                                                                                                |
|          | FvFspS.fv         | FvPostMemorySilicon.fv        |                                                                                                                                |
|          |                   | (child FV)                    |                                                                                                                                |
|          |                   | Additional Components         |  Post-memory silicon initialization components                                                                 |
|          |                   | Additional components         |                                                                                                                                |



---
@title[Stage 1 Modules]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 1 Modules</b>)</span><span style="font-size:0.75em;" ><br> - Example <font face="Consolas">SecCore.efi</font></span></p>


@snap[north-west span-100 ]
<br>
<br>
<p style="line-height:70%"><span style="font-size:0.8em; font-family:Consolas;" ><br> 
<font face="Arial">Producing Package -  </font>UefiCpuPkg<br><br>
<font face="Arial">Libraries Consumed -  </font>PlatformSecLib, SerialPortLib
<br></span></p>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Library</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:50%"><span style="font-size:0.65em" ><b>API Definition</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:50%"><span style="font-size:0.65em" ><b>Producing Pkg</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Description</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > PlatformSecLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > UefiCpuPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:010%"><span style="font-size:0.45em" >Reset vector and SEC initialization code.  </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > SerialPortLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MdeModulePkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > Board&lt;X&gt;Pkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:030%"><span style="font-size:0.45em" > SIO vendor specific initialization to enable serial port. </span></p></td>
	</tr>
</table>
<br>
@snapend




Note:


Only modules found in the BoardPkg should be modified for board porting. MinPlatformPkg and other common package contents must not be directly modified. BoardPkg and SiliconPkg modules will have multiple instances to support different boards and different silicon.


Board porting will require creation of libraries identified as produced by the BoardPkg. Depending on the board, there may be existing libraries that are sufficient for a board, so it is important to assess the utility of existing library instances when developing board support.



---
@title[Stage 1 Platform Libraries]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 1 Platform Libraries</b>)</span><span style="font-size:0.75em;" ></b></span></p>


@snap[north-west span-100 ]
<br>
<br>
<table id="recTable-1">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Item</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>API Definition</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Producing Pkg</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Description</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > BoardInitLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > BoardPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:01%"><span style="font-size:0.4em" > Board initialization library. </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > ReportFvLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:020%"><span style="font-size:0.4em" > Installs platform firmware volumes. </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > SerialPortLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MdeModulePkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > BoardPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:030%"><span style="font-size:0.4em" >  SIO vendor specific initialization to enable serial port.</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > SiliconPolicyInitLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > IntelSiliconPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > SiliconPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:030%"><span style="font-size:0.4em" > Provides default silicon configuration policy data. </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > SiliconPolicyUpdateLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > IntelSiliconPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > BoardPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:030%"><span style="font-size:0.4em" > Provides board updates to silicon configuration policy data. </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > PlatformSecLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > UefiCpuPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em" >  Reset vector and SEC initialization code.</span></p></td>
	</tr>
</table>
<br>
@snapend




Note:

https://github.com/tianocore-docs/edk2-MinimumPlatformSpecification/blob/master/3_stage_1_minimum_debug/33_modules.md#332-platform-architecture-libraries

To find the Libraries for the Platform specific code
1 Search the Work space .DSC files for the string of the library
2 Open the .DSC files associated with the platform
3 Determine which Library is used and that should have the build path in the workspace.

Board porting will require creation / porting of libraries identified as produced by the BoardPkg. Depending on the board, there may be existing libraries that are sufficient for a board, so it is important to assess the utility of existing library instances when developing board support.


---?image=assets/images/slides/Slide30.JPG
@title[How to search for Libraries in the Workspace]
<p align="right"><span class="gold" >@size[1.1em](<b>How to search for Libraries in the Workspace</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-67 ]
<br>
<br>
<br>
<br>
<ul style="list-style-type:none; line-height:0.7;">
  <li><span style="font-size:0.7em" >1. Search the workspace .DSC files for the <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;string of the library<br></span> </li><br>
  <li><span style="font-size:0.7em" >2. Open the .DSC files associated with the <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;open board platform project<br></span> </li><br>
  <li><span style="font-size:0.7em" >3. Determine which Library is used and that <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;should have the build path in the workspace<br></span> </li><br>
  <li><span style="font-size:0.7em" >4. DSC file will have similar to:</span> </li>
  <li><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;&nbsp;&nbsp;@color[yellow](SomeLib)|Path_to_the_Library_used.inf</span> </li>
</ul>

@snapend



Note:
http://sustituciondepuestosclaves.wikispaces.com/Metodo+de+Sustitucion+de+Puestos+Claves 

Another Note: use Regular expressions to find multiple strings:
Example, to fine the strings “Hob” and “Serial”

    Serial.*Hob|Hob.*Serial  

reg exp to find string1 "Serial" string2 "Hob"



---?image=assets/images/slides/Slide31.JPG
@title[Platform SEC Lib - Kabylake ]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform SEC Lib - Kabylake </b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[south-west span-49 ]
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[south-east span-49 ]
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-west span-100 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.8em;">
Search the board platform .DSC file for where the @color[#A8ff60](<font face="Consolas">PlatformSecLib</font>) is in the Platform-Board Tree
</span></p>
<p style="line-height:50%" align="left" ><span style="font-size:0.7em;">
DSC FILE:<br>
<font face="Consolas">
@size[.7em](@color[#A8ff60](PlatformSecLib)|MinPlatformPkg/FspWrapper/Library/\ )<br>&nbsp;&nbsp;
  @size[.7em](SecFspWrapperPlatformSecLib/@color[yellow](SecFspWrapperPlatformSecLib.inf))
</font>
<br>
<br>
@size[.8em](Directory:)
</span></p>
@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br><br>
Library/SecFspWrapperPlatformSecLib/<br>&nbsp;&nbsp;
    FsptCoreUpd.c<br>&nbsp;&nbsp;
    FspWrapperPlatformSecLib.c<br>&nbsp;&nbsp;
    Platforminint.c<br>&nbsp;&nbsp;
    @color[yellow](SecFspWrapperPlatformSecLib.inf)<br>&nbsp;&nbsp;
    SecGetPerformance.c<br>&nbsp;&nbsp;
    SecPlatforminformation.c<br>&nbsp;&nbsp;
    SecRamInitData.c<br>&nbsp;&nbsp;
    SecTemRamDone.c<br>&nbsp;&nbsp;

<br>&nbsp;&nbsp;
</span></p>
@snapend


@snap[north-east span-45 ]
<br>
<br>
<br>
<br>
<br>
<br><p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br><br><br><br>
IA32/<br>&nbsp;&nbsp;
   fsp.h<br>&nbsp;&nbsp;
   PeiCoreEntry.nasm<br>&nbsp;&nbsp;
   @color[#A8ff60](SecEntry.nasm)<br>&nbsp;&nbsp;
   Stack.nasm<br>&nbsp;&nbsp;
<br>&nbsp;&nbsp;
</span></p>
@snapend



@snap[north-east span-28 fragment ]
<br>
<br>
<br>
<br>
<br>
<br><p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br><br><br><br>
<br>&nbsp;&nbsp;
   <br>&nbsp;&nbsp;
   <br>&nbsp;&nbsp;
   &nbsp;&nbsp;@fa[arrow-left fa-2x gp-bullet-yellow]<i>@size[.7em](&nbsp;&nbsp;_ModuleEntryPoint)</i><br>&nbsp;&nbsp;
   <br>&nbsp;&nbsp;
<br>&nbsp;&nbsp;
</span></p>
@snapend



Note:

Since we now know that the SEC code is in the FV –FvPreMemory and the module is SecCore.efi and the Libraries for SecCore.efi are PlatformSecLib and SerialPortLib we can search the board platform .DSC file for where the PlatformSecLib is in the Platform-Board Tree

The ModuleEntryPoint is in SecEntry.nasm

Entry point after reset vector is platform specific
SecEntry.asm
ModuleEntryPoint

http://4.bp.blogspot.com/-_yn2oKMT4i4/UUdVkp1rBuI/AAAAAAAAAlw/lGtpuQsmqOk/s1600/icon_detective.png

Of this slide we have what we need to port our new package platform for the SEC  phase.
We find this code in our new platform package directory under the library directory under the directory called something like new platform SEC lib. Under this directory we see that we have a “C”, “H” and Inf files, And we also see another directory, in our case for our example platform, we have an IA32 directory. This directory would have assembly language source files for our port.

Let’s take a look at the details of these files:
After the reset vector and after those initial architecture specific instructions, a jump will be made into the platform SEC library code. The Entry point after common reset vector is platform specific in SecEntry.nasm  with the label _ModuleEntryPoint.

The file SecEntry.nasm – calls the entry for setting up our temporary memory and the Application Processors
We will need to look at the code at the label SecEntry.nasm where we would  make a call to set up our temporary memory and the cache as RAM. 

From reset vector to _ModuleEntryPoint
;   Transition to non-paged flat-model protected mode from a
;   hard-coded GDT that provides exactly two descriptors.
;   This is a bare bones transition to protected mode only
;   used for a while in PEI and possibly DXE.
;
;   After enabling protected mode, a far jump is executed to
;   transfer to PEI using the newly loaded GDT.

---?image=assets/images/slides/Slide32.JPG
@title[Establish Temporary Memory ]
<p align="right"><span class="gold" >@size[1.1em](<b>Establish Temporary Memory </b>)</span><span style="font-size:0.75em;" ><br>Call to FSP API </span></p>


@snap[north-west span-60 ]
<br>
<br>
<p style="line-height:80%" align="left" ><span style="font-size:0.8em;">
Call to TempRamInit API  located in the FSP Binary module
</span></p>
@snapend


@snap[west span-40 fragment]
@box[bg-green-pp text-black waved my-box-pad2 ](<p style="line-height:70%" align="center"><span style="font-size:0.65em; font-family:Consolas;" >@size[1.3em](FSP-T)<br><br>TempRamInit API<br><br>&nbsp;</span></p>)
@snapend



@snap[south-west span-60 fragment]
<p style="line-height:70%" align="left"><span style="font-size:0.55em; font-family:Consolas;" >
TempRamInit Api 
</span></p>
<ul style="list-style-type:disc; line-height:0.6;">
  <li><span style="font-size:0.55em" >Initializes T-RAM silicon functionality<br>@size[.7em]( &nbsp;&nbsp;&nbsp;&nbsp;- No Evection mode / Cache As Ram)</span> </li>
  <li><span style="font-size:0.55em" >Tests T-RAM functionality</span> </li><br>
</ul>
<br>
<br>
@snapend


Note:

The Temp memory is set up through the FSP TempRamInit API

Call to the TempRamInit API is made that is located in the FSP Binary module
The  FSP binary is rebased for the FvFspT Firmware Volume.

Boot Loader must pass valid CAR region for FSP stack use through FSPM_UPD.FspmArchUpd.StackBase and
FSPM_UPD.FspmArchUpd.StackSize UPDs.
The minimum FSP stack size required for this revision of FSP is 160KB, stack base is 0xFEF17F00 by default. (from KabyLake FSP integraton Guide (KBLK IG)

At the end of TempRamExit the original code and data caching are disabled. FSP will reconfigure all MTRRs as
described in the table below for performance optimization.
Memory range Cache Attribute
0x00000000 - 0x0009FFFF Write back
0x000C0000 - Top of Low Memory Write back
0xFF800000 - 0xFFFFFFFF (Flash region) Write protect
0x1000000000 - Top of High Memory Write back
If the boot loader wish to reconfigure the MTRRs differently, it can be overridden immediately after this API call.


---
@title[Transition to PEI Entry Point ]
<p align="right"><span class="gold" >@size[1.1em](<b>Transition to PEI Entry Point </b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:80%" align="left" ><span style="font-size:0.75em;">
SecMain calls the entry point into PEI Core
</span></p>

```
Secmain(  
{ . . .
  // Transfer the control to the PEI core
  ASSERT (PeiCoreEntryPoint != NULL);
  (*PeiCoreEntryPoint) (SecCoreData, PpiList); 
  UNREACHABLE ();

```

<p style="line-height:70%" align="left" ><span style="font-size:0.75em;">
<font face="Consolas">@size[.8em](PeiCore)</font> is the <font face="Consolas">@size[.8em](PeiCoreEntryPoint)</font> in the <font face="Consolas">@size[.8em](FvPreMemory)</font>  Firmware Volume:<Br>
 <font face="Consolas">@size[.7em](@color[yellow](edk2/MdeModulePkg/Core/Pei/PeiMain PeiMain.c))</font>
</span></p>

```
EFIAPI
PeiCore (
  IN CONST EFI_SEC_PEI_HAND_OFF        *SecCoreDataPtr,
  IN CONST EFI_PEI_PPI_DESCRIPTOR      *PpiList,
  IN VOID                              *Data
  )
{


```

Note:

Same ase slide


---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Modules - Stage 1 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Modules <br>- Stage 1</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-49 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
MinPlatformPkg/<br>&nbsp;&nbsp;
  Include/<br>&nbsp;&nbsp;&nbsp;&nbsp;
     Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	   @color[yellow](BoardnitLib.h)<br>&nbsp;&nbsp;
  Library/<br>&nbsp;&nbsp;
  . . .<br>&nbsp;&nbsp;
  @color[cyan](PlatformInit/)<br>&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitPei/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	  PlatformInitPreMem/<br>&nbsp;&nbsp;
<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-46 ]
<br>
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
BoardDetect&lpar;&rpar;<br>
BoardDebugInit&lpar;&rpar;<br>
BoardBootModeDetect&lpar;&rpar;<br>
BoardInitBeforeMemoryInit&lpar;&rpar;<br>
<br>&nbsp;&nbsp;
</span></p>
@snapend




@snap[north-east span-72 fragment]
<br>
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
<br>
<br>
<br>
<font face="Arial">@size[1.7](@color[#A8ff60]( <b>&larr;</b>)) &nbsp;&nbsp;// hooks</font><br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-46 ]
<br>
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
BoardDetect&lpar;&rpar;<br>
BoardDebugInit&lpar;&rpar;<br>
BoardBootModeDetect&lpar;&rpar;<br>
BoardInitBeforeMemoryInit&lpar;&rpar;<br>
<br>&nbsp;&nbsp;
</span></p>
@snapend




@snap[south span-95 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:70%"><span style="font-size:0.8em">PlatformInit folder <font face="Consolas">@size[.8em](PlatformInit)</font> controls<br> the platform initialization flow<br>&nbsp;</span></p>)
@snapend


Note:

The PlatformInit folder (Intel/MinPlatformPkg/PlatformInit) - PlatformInitPei, PlatformInitDxe and PlatformInitSmm control the platform initialization flow. 

Because this flow needs to involve the board initialization,  there is a set of  board hook points defined in BoardInitLib (MinPlatformPkg/Include/Library/BoardInitLib.h) 



---?image=assets/images/slides/Slide37.JPG
@title[Hook - Board Detection ]
<p align="right"><span class="gold" >@size[1.1em](<b>Hook - Board Detection </b>)</span><span style="font-size:0.75em;" ><br> - Kabylake example</span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
MinPlatformPkg/<br>&nbsp;&nbsp;
 . . .<br>&nbsp;&nbsp;
  PlatformInit/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitPei -&gt;  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         PlatformInitPreMem.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			 @color[cyan](BoardDetect&lpar;&rpar;)<br>
KabylakeOpenBoardPkg/<br>&nbsp;&nbsp;
 . . .<br>&nbsp;&nbsp;
  KabylakeRvp3/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      BoardInitLib -&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        PeiBoardInitPreMemLib.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			 @color[cyan](BoardDetect&lpar;&rpar;)  <br>&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;
        PeiKabylakeRvp3Detect.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			 @color[yellow](KabylakeRvp3BoardDetect&lpar;&rpar;)

<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-47 ]
<br>
<br>
<br>
<p style="line-height:65%" align="left" ><span style="font-size:0.7em; ">
Uses PCD Library calls to set / get Board SKU for Storing Board ID<br>
   <font face="Consolas">@size[.8em](LibPcdGetSku&lpar;&rpar; & LibPcdSetSku&lpar;&rpar;)</font><br><br>

<font face="Consolas">@size[.8em](KabylakeRvp3BoardDetect&lpar;&rpar;)</font> function reads Board ID from embedded controller (EC) using the LPC bus  <br><br>
@size[.8em](<font face="Consolas">LibPcdSetSku&lpar;&rpar;</font> stores Board ID)<br>
@size[.8em](<font face="Consolas">LibPcdGetSku&lpar;&rpar;</font> used from that point on)

<br>&nbsp;&nbsp;
</span></p>
@snapend



Note:



In order to determine which board specific driver needs to run and which does not need to run, there must be some code to detect the board type. 
The board detection code is board specific. It should be under the board specific directory 

Uses PCD calls to set / get Board Sku for Storing Board ID
	LibPcdGetSku() & LibPcdSetSku()

For the Kabylake example the lower function KabylakeRvp3BoardDetect() will read the ID from the EC using the LPC bus. 
Then is updates LibPcdSetSku() with the Board ID
LibPcdGetSku() can then be used elsewhere

The EC implements an embedded controller interface at ports 0x60/0x64 and a ACPI compliant
system management controller at ports 0x62/0x66. Port 0x66 is the command and status port,
port 0x62 is the data port.

Another NOTE: The SKU ID check should only happen in board specific drivers. The SKU ID check is NOT allowed in any common board code or common platform code. 


SkuIds is a special usage of PCD. It can support multiple configurations generated at build time, and it supports runtime selection to make one configuration take effect finally. 
Multi-sku PCD concept is defined by PI specification Volume 3, Chapter 8 PCD, EFI_PCD_PROTOCOL.SetSku () 


---
@title[Configuration Multi-SKU PCD – Board ID  ]
<p align="right"><span class="gold" >@size[1.1em](<b>Configuration Multi-SKU PCD – Board ID </b>)</span><span style="font-size:0.8em;" ></span></p>

@snap[north-west span-49 ]
<br>
<br>
<br>
<br>

@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-48 ]
<br>
<br>
<br>
<br>

@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-west span-48 ]
<p style="line-height:70%" align="left" ><span style="font-size:0.8em;" ><br><br>
@color[cyan](DSC File – SKU Set at BUILD time)
</span></p>

<p style="line-height:35% " align="left"></span><span style="font-size:0.4em; font-family:Consolas;" ><br>&nbsp;&nbsp;
 .&nbsp;.&nbsp;.<br>&nbsp;&nbsp;
SKUID_IDENTIFIER = ?<br>&nbsp;&nbsp;
<br>&nbsp;&nbsp;
[SkuIds]<br>&nbsp;&nbsp;
0|DEFAULT<br>&nbsp;&nbsp;
4|BoardX<br>&nbsp;&nbsp;
0x42|BoardY<br>&nbsp;&nbsp;
<br>&nbsp;&nbsp;
[PcdsDynamicDefault.common.@color[yellow](BoardX)]<br>&nbsp;&nbsp;
gBoardModuleTokenSpaceGuid.PcdGpioPin|0x8<br>&nbsp;&nbsp;
gBoardModuleTokenSpaceGuid.PcdGpioInitValue|\<br>&nbsp;&nbsp;&nbsp;&nbsp;
        &lbrace;0x00, 0x04, 0x02, 0x04, ...&rbrace;<br>&nbsp;&nbsp;
<br>&nbsp;&nbsp;
[PcdsDynamicDefault.common.@color[yellow](BoardY)]<br>&nbsp;&nbsp;
gBoardModuleTokenSpaceGuid.PcdGpioPin|0x4<br>&nbsp;&nbsp;
gBoardModuleTokenSpaceGuid.PcdGpioInitValue|\<br>&nbsp;&nbsp;&nbsp;&nbsp;
        &lbrace;0x00, 0x02, 0x01, 0x02, ...&rbrace;<br>&nbsp;&nbsp;
</span></p> 
@snapend


@snap[north-east span-47 ]
<p style="line-height:70%" align="left" ><span style="font-size:0.8em;" ><br><br>
@color[cyan](SKU PCD Set Dynamically)
</span></p>
<br>
<p style="line-height:35% " align="left"></span><span style="font-size:0.4em; font-family:Consolas;" >
&nbsp;&nbsp;
BoardXBoardDetect( VOID)<br>&nbsp;&nbsp;
&lbrace;<br>&nbsp;&nbsp;
. . .<br>&nbsp;&nbsp;&nbsp;&nbsp;
  if (@color[yellow](LibPcdGetSku) () != 0) &lbrace; <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    return EFI_SUCCESS;<br>&nbsp;&nbsp;&nbsp;&nbsp;
  &rbrace; <br>&nbsp;&nbsp;&nbsp;&nbsp;
  if (IsBoardX ()) &lbrace; <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     @color[yellow](LibPcdSetSku) (BoardIdIsBoardX);<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     ASSERT (LibPcdGetSku() == <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
              BoardIdIsBoardX);<br>&nbsp;&nbsp;&nbsp;&nbsp;
  &rbrace;<br>&nbsp;&nbsp;&nbsp;&nbsp;
  return EFI_SUCCESS;<br>&nbsp;&nbsp;
&rbrace;<br>&nbsp;&nbsp;
</span></p> 
@snapend



@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:70%"><span style="font-size:0.8em">PCD Determines Board ID at Build time<br>&nbsp;</span></p>)
@snapend


Note:
SkuIds is a special usage of PCD. It can support multiple configurations generated at build time, and it supports runtime selection to make one configuration take effect finally. 

Multi-sku PCD concept is defined by PI specification Volume 3, Chapter 8 PCD, EFI_PCD_PROTOCOL.SetSku (). 

The SKU PCD is actually a dynamic PCD. During boot, the board detection takes the responsibility to set the SKU. Once the SKU PCD is set, the configuration associated with this SKU takes effect immediately 

---?image=assets/images/slides/Slide37.JPG
@title[Board Debug Initialization ]
<p align="right"><span class="gold" >@size[1.1em](<b>Board Debug Initialization </b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/KabylakeOpenBoardPkg/<br>&nbsp;
 . . .<br>&nbsp;
 KabylakeRvp3/<br>&nbsp;&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;
    BoardInitLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;
     PeiKabylakeRvp3InitPreMemLib.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       @color[yellow](KabylakeRvp3DebugInit&lpar;&rpar;)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  		  @color[cyan](EarlySiliconInit&lpar;&rpar;)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       . . .<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       @color[yellow](KabylakeRvp3BoardBootModeDetect&lpar;&rpar;)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
		 return <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
		 BOOT_WITH_FULL_CONFIGURATION<br>&nbsp;&nbsp;<br>

Silicon/Intel/KabylakeSiliconPkg/<br>&nbsp;&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiliconInitLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      SiliconInitPreMem.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        @color[cyan](EarlySiliconInit&lpar;&rpar;) <br>&nbsp;&nbsp;

<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-47 ]
<br>
<br>
<p style="line-height:65%" align="left" ><span style="font-size:0.7em; ">
Once Board detection is successful, the next step is Board initialization. <br><br>
Kabylake example calls :
   <font face="Consolas">@size[.8em](EarlySiliconInit )</font>
   <br><br>
   - Early Platform PCH initialization<br><br>
   - Boot Mode Detect <br>&nbsp;&nbsp;– @size[.8em](example returns Boot with full <br>&nbsp;&nbsp;&nbsp;&nbsp;configuration )
</span></p>
@snapend



Note:


### Early Platform PCH initialization
- Program ACPI BASE
- Program PWRM BASE
- Program TCO BASE if it is present and not locked
- LPC I/O Configuration
- Enable the upper 128-byte bank of RTC RAM
- Disable the Watchdog timer expiration from causing a system reset 
- Halt the TCO timer
- Disable SERR NMI and IOCHK# NMI in port 61
- Program timer 1 as refresh timer

---?image=assets/images/slides/Slide37.JPG
@title[Board Init Before Memory Init]
<p align="right"><span class="gold" >@size[1.1em](<b>Board Init Before Memory Init</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-51 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/KabylakeOpenBoardPkg/<br>&nbsp;
 . . .<br>&nbsp;
 KabylakeRvp3/<br>&nbsp;&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;
    BoardInitLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;
     PeiKabylakeRvp3InitPreMemLib.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       @color[yellow](KabylakeRvp3BoardInitBeforeMemoryInit&lpar;&rpar;)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  		 KabylakeRvp3InitPreMem ()<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  		 I2CGpioExpanderInitPreMem()<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 		 GpioInitPreMem ()<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 		 SioInit ()<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
		 @color[cyan](SiliconInit&lpar;&rpar;)<br>
Silicon/Intel/KabylakeSiliconPkg/<br>&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiliconInitLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      SiliconInitPreMem.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        @color[cyan](SiliconInit&lpar;&rpar;) <br>&nbsp;&nbsp;

<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-46 ]
<br><br>
<br>
<p style="line-height:65%" align="left" ><span style="font-size:0.7em; ">
Board Initialization before Memory Initialization
 <br><br><br><br>
The board specific initialization may include: 
</span></p>
@snapend


@snap[north span-5 ]
<br>
<br><br>
<br>
<br><br><br><br>
<br>
<ul style="list-style-type:none; line-height:0.7;">
  <li><span style="font-size:0.65em" >&nbsp;&nbsp;&nbsp;1. <br>&nbsp;</span> </li>
  <li><span style="font-size:0.65em" >&nbsp;&nbsp;&nbsp;2. <br>&nbsp;</span> </li>
  <li><span style="font-size:0.65em" >&nbsp;&nbsp;&nbsp;3. </span> </li>
</ul>
@snapend


@snap[north-east span-46 ]
<br>
<br>
<br><br><br><br>
<br><br>
<br>
<ul style="list-style-type:none; line-height:0.7;">
  <li><span style="font-size:0.65em" >Invoke a set of PCD for policy initialization later. </span> </li>
  <li><span style="font-size:0.65em" >Configure the hardware devices (such as GPIO, SIO) </span> </li>
  <li><span style="font-size:0.65em" >Silicon Initialization – i.e. PCH  </span> </li>
</ul>
@snapend



Note:

Once Board detection is successful, the next step is Board initialization. 
If the final BIOS image only needs to support one board, the board code can just implement a set of Board initialization API’s directly 



---?image=assets/images/slides/Slide37.JPG
@title[GPIOs – Stage 1]
<p align="right"><span class="gold" >@size[1.1em](<b>GPIOs – Stage 1</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-51 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/KabylakeOpenBoardPkg/<br>&nbsp;
 . . .<br>&nbsp;
 KabylakeRvp3/<br>&nbsp;&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;
    BoardInitLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;
     PeiKabylakeRvp3InitPreMemLib.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       @color[yellow](KabylakeRvp3BoardInitBeforeMemoryInit&lpar;&rpar;)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  		 KabylakeRvp3InitPreMem ()<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  		 I2CGpioExpanderInitPreMem()<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 		 @color[cyan](GpioInitPreMem &lpar;&rpar;)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 		 SioInit ()<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
		 SiliconInit&lpar;&rpar;<br>
Silicon/Intel/KabylakeSiliconPkg/<br>&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    PeiDxeSmmGpioLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      GpioInit.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        @color[cyan](GpioConfigureSklPch &lpar;&rpar;) <br>&nbsp;&nbsp;

<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-46 ]
<br><br>
<br>
<p style="line-height:65%" align="left" ><span style="font-size:0.7em; ">
If GPIOs need to be Initialized pre-memory then the hook <font face="Consolas">GpioInitPreMem()</font> calls the silicon library for GPIOs<br><br>
Example for Kabylake PCH GPIO pins
Table: <font face="Consolas">KabylakeRvp3GpioTable.c</font>
</span></p>
@snapend




Note:

procedure  GpioConfigurePads calls GpioConfigureSklPch()
 will initialize multiple GPIO pins. Use GPIO_INIT_CONFIG structure.
  Structure contains fields that can be used to configure each pad.
  Pad not configured using GPIO_INIT_CONFIG will be left with hardware default values.
  Separate fields could be set to hardware default if it does not matter, except
  GpioPad and PadMode.
  Some GpioPads are configured and switched to native mode by RC, those include:
  SerialIo pins, ISH pins, ClkReq Pins


---
@title[Silicon Policy – Stage 1]
<p align="right"><span class="gold" >@size[1.1em](<b>Silicon Policy – Stage 1</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-51 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/MinPlatformPkg/<br>&nbsp;
 . . .<br>&nbsp;
 PlatformInit/<br>&nbsp;&nbsp;&nbsp;
  SiliconPolicyPei/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     SiliconPolicyPeiPreMem.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       @color[cyan](SiliconPolicyInitPreMem&lpar;&rpar;)<br><br>

Silicon/Intel/KabylakeSiliconPkg/<br>&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;
      PeiSiliconPolicyInitLibFsp<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         PeiFspPolicyInitLib.c  <br>&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;
          @color[cyan](SiliconPolicyInitPreMem&lpar;&rpar;)
<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-46 ]
<br><br>
<br>
<p style="line-height:65%" align="left" ><span style="font-size:0.7em; ">
Performs silicon pre-mem policy initialization.<br><br>
The meaning of Policy is defined by silicon code.<br><br>
Input Policy should be <font face="Consolas">FspmUpd</font>. <br><br>
Value of FspmUpd has been initialized by FSP binary default value
<br><br>
</span></p>
@snapend

@snap[south-west span-40 fragment]
@box[bg-green-pp text-black waved my-box-pad2 ](<p style="line-height:70%" align="center"><span style="font-size:0.65em; " >@size[1.3em](FSP-M)<br>&nbsp;<br>Fsp Silicon Policy Update<br>Pre&nbsp;Mem<br>&nbsp;</span></p>)
@snapend



Note:
Performs silicon pre-memory policy update.

The meaning of Policy is defined by silicon code.

It could be the raw data, a handle, a PPI, etc.

The input Policy must be returned by SiliconPolicyDonePreMemory().

1) In FSP path, the input Policy should be FspmUpd.

A platform may use this API to update the FSPM UPD policy initialized
by the silicon module or the default UPD data.


The output of FSPM UPD data from this API is the final UPD data.


---
@title[Debug Configuration - Serial Port]
<p align="right"><span class="gold" >@size[1.1em](<b>Debug Configuration - Serial Port</b>)</span><span style="font-size:0.75em;" ></span></p>

<p style="line-height:65%" align="left" ><span style="font-size:0.7em; ">
Serial port parameters come from the board and are used for debug features, serial input/output devices supporting local or remote consoles, and OS level debuggers<br><br>
Library – <font face="Consolas">@color[yellow](SerialPortLib)</font> find in workspace used by board .dsc<br><br>
Serial port configuration options consumed by <font face="Consolas">@color[yellow](SerialPortLib)</font> <br><br>
<font face="Consolas">@color[yellow](SerialPortLib)</font> is used by the <font face="Consolas">@color[yellow](StatusCodeHandlerPei.inf)</font> component to initialize and 
display messages to a serial port<br><br>
Serial port configuration options are published via @color[yellow](PCH_SERIAL_IO_CONFIG) used by <font face="Consolas">@color[yellow](PeiPchPolicyLib)</font>  <br>
&nbsp;&nbsp;&nbsp;&nbsp;<font face="Consolas">@size[.8em](Silicon/Intel/KabylakeSiliconPkg/Pch/Library/PeiPchPolicyLib)</font>
</span></p>

Note:

Serial port parameters come from the board
and are used for debug features, serial input/output devices supporting local or remote
consoles, and OS level debuggers

Serial port configuration options are consumed by the SerialPortLib library class implementation.
SerialPortLib library class is used by the StatusCodeHandlerPei.inf component to initialize and display messages to a serial port.

Find the SerialPortLib for the board code
To find the Libraries for the Platform specific code
1. Search the Work space .DSC files for the string of the library
2. Open the .DSC files associated with the platform
3. Determine which Library is used and that should have the build path in the workspace.

Kabylake uses SerialPortLib default core from MdeModulePkg/Library/BaseSerialPortLib16550/BaseSerialPortLib16550.inf
Kabylake uses StatusCodeHandlerPei from MdeModulePkg/Universal/StatusCodeHandler/Pei/StatusCodeHandlerPei.inf

Find library for creating Serial for the Hobs to pass to next phase. For Kabylake it is PCH_SERIAL_IO_CONFIG used by PeiPchPolicyLib for Hobs  located: Silicon/Intel/KabylakeSiliconPkg/Pch/Library/PeiPchPolicyLib

The PCH_SERIAL_IO_CONFIG block provides the configurations to set the Serial IO controllers
  to Acpi devices or Pci controllers, and also set the interrupt type to Acpi or Pci
  through Policy.


---
@title[Debug Configuration PCDs - Serial Port]
<p align="right"><span class="gold" >@size[1.1em](<b>Debug Configuration PCDs - Serial Port</b>)</span><span style="font-size:0.75em;" ></span></p>



@snap[north-west span-100 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>

<p style="line-height:45%" align="left" ><span style="font-size:0.4em; font-family:Consolas;"><br>
gEfiMdeModulePkgTokenSpaceGuid.PcdSerialBaudRate - <font face="Arial">Baud rate for the 16550 serial port</font><br>
gEfiMdeModulePkgTokenSpaceGuid.PcdSerialUseMmio - <font face="Arial">Enable serial port MMIO addressing </font><br>
gEfiMdeModulePkgTokenSpaceGuid.PcdSerialUseHardwareFlowControl - <font face="Arial">Enable serial port HW flow control  </font><br>
gEfiMdeModulePkgTokenSpaceGuid.PcdSerialDetectCable - <font face="Arial">Enable blocking Tx if no cable  </font><br>
gEfiMdeModulePkgTokenSpaceGuid.PcdSerialRegisterBase - <font face="Arial">Register the serial port base address </font><br>
gEfiMdeModulePkgTokenSpaceGuid.PcdSerialLineControl - <font face="Arial">Serial port line control configuration  </font><br>
gEfiMdeModulePkgTokenSpaceGuid.PcdSerialFifoControl - <font face="Arial">Serial port FIFO control  </font><br>
gMinPlatformPkgTokenSpaceGuid.PcdSecSerialPortDebugEnable - <font face="Arial">Enable serial port debug in SEC phase </font><br>
<br>
<br>
<br>
<font face="Arial">@size[1.4em](Debug configuration PCDs) </font><br>
gEfiMdePkgTokenSpaceGuid.PcdFixedDebugPrintErrorLevel - <font face="Arial">Control optimization based on debug print level - messaage type</font><br>
gEfiMdePkgTokenSpaceGuid.PcdDebugPropertyMask - <font face="Arial">Control DebugLib behavior  </font><br>
gEfiMdePkgTokenSpaceGuid.PcdDebugPrintErrorLevel - <font face="Arial">Control run time debug print level </font><br>
gEfiMdePkgTokenSpaceGuid.PcdReportStatusCodePropertyMask - <font face="Arial">Control display of status codes </font><br>
</span></p>
@snapend


Note:

slide show the PCDs for the serial port for configuration 

also shown are the debug configuration PCDs


---
@title[Stage 1 Checklist ]
<p align="center"><span class="gold" >@size[1.1em](<b>Stage 1 Checklist </b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; ">Steps to enable a board for Stage 1.
</span></p>

@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

@snap[north-east span-98 ]
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.7em; "> <br><br>
 1. Copy the EDK II packages to a local workspace  <br>
 2. Select the correct Intel® FSP & review requirements  <br>
 3. Get silicon initialization requirements for the given board. <br>
 4. Customize the silicon initialization solution to the board-specific <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;requirements. <br>
 5. Determine other firmware and software components <br>
 6. Determine board-specific information required to fetch code and <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;show debug output. <br>
 7. Copy a reference <font face="Consolas">@size[.8em](GenerationOpenBoardPkg/BoardXxx)</font> and update the <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;board interfaces in Required Functions. <br>
   &nbsp;&nbsp;&nbsp;&nbsp;- serial port initialization code in <font face="Consolas">@size[.8em](PlatformHookSerialPortInitialize &lpar;&rpar;)</font> at<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  <font face="Consolas">@size[.8em](BoardPkg/Library/BasePlatformHookLib.)</font> <br>
   &nbsp;&nbsp;&nbsp;&nbsp;- Add Board detection code in <font face="Consolas">@size[.8em](BoardDetect &lpar;&rpar;)</font>
</span></p>
@snapend

Note:

Steps to enable a board for Stage I.
Copy the EDK II packages locally to the workspace.
Select silicon initialization solution .i.e. Intel® FSP. & Review the requirements for the silicon initialization solution.
Gather the silicon initialization requirements for the given board.
Customize the silicon initialization solution to configure the system to the board-specific requirements
  - For Intel® FSP, this includes setting minimal policy configuration.
  - For other silicon solutions, similar parameter customization may be needed if the silicon solution is not written for a particular system design.
6, Determine other firmware and software components required for the system to function properly.
  - For an Intel platform, this may include firmware images such as the appropriate microcode patch, EC firmware image, power management controller firmware, and others.
  - Additional third-party add-in components such as specific UEFI drivers may also be required.
7. Determine board-specific information required to fetch code and show debug output.
  - This includes details such as the NVRAM layout and strap information.
8. Copy a reference GenerationOpenBoardPkg/BoardXXX and update the board
interfaces in Required Functions.
  - Add serial port initialization code in PlatformHookSerialPortInitialize () at 				BoardPkg/Library/BasePlatformHookLib.
  - This is SIO related code.
ii. Add Board detection code in BoardDetect ()


BoardPkg/BoardInitLib/PeiBoardXXXInitPreMemoryLib.c`
If the project only supports one board, this function can return directly.
2. Add Board pre-memory debug initialization code in BoardDebugInit () ,
BoardPkg/BoardInitLib/PeiBoardXXXInitPreMemoryLib.c.
i. This is for debug channel related initialization.
3. Audit BoardPkg/Stage1.dsc, ensure all PCDs in the Configuration section are correct for
your board.
i. Set gMinPlatformPkgTokenSpaceGuid.PcdBootStage = 1
ii. Follow "Debug Lib Selection" to enable serial debug capability.
4. Audit all other PCD settings in the board DSC file to verify the values are correct for
your board.
5. Verify the flash layout is compliant with this specification.
6. Verify the required binaries will be included in the image produced in the build.
7. Verify the code execution path for Stage I will only perform the actions required to
achieve debug output.
8. Boot the system, collect the debug log, and verify the test point results are correct.



---
@title[Stage 1 Checklist 02 ]
<p align="center"><span class="gold" >@size[1.1em](<b>Stage 1 Checklist<br>- Board Pre-mem Lib </b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; ">
Kabylake -<br>
<font face="Consolas">@size[.7em](KabylakeOpenBoardPkg/KabylakeRvp3/Library/BoardInitLib/@color[yellow](PeiBoardInitPreMemLib))</font>
</span></p>

@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

@snap[north-east span-98 ]
<br>
<br>
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.7em; "> <br>
 1. Add Board pre-memory debug initialization code in <font face="Consolas">@size[.8em](BoardDebugInit&lpar;&rpar;)</font>  <br>
 2. Ensure all PCDs in the Configuration section are correct (i.e. Serial debug) <br>
 3. Verify values of other PCDs are correct <br>
 4. Verify the flash layout is compliant <br>
 5. Verify the required binaries  included in the build <br>
 6. Verify debug output during the code execution path for Stage 1 <br>
 7. Verify the test point results  are correct <br>
</span></p>

<p style="line-height:70%" align="left" ><span style="font-size:0.45em; ">
<a href="https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/3_stage_1_minimum_debug/39_test_point_results.html">EDK II Open Platform Spec Test points Stage 1</a>
</span></p>

@snapend

Note:
BoardPkg/BoardInitLib/PeiBoardXXXInitPreMemoryLib.c`

1. If the project only supports one board, this function can return directly.
2.  Add Board pre-memory debug initialization code in BoardDebugInit () , BoardPkg/BoardInitLib/PeiBoardXXXInitPreMemoryLib.c. - This is for debug channel related initialization.
3.  Audit BoardPkg/Stage1.dsc, ensure all PCDs in the Configuration section are correct for
your board. - Set gMinPlatformPkgTokenSpaceGuid.PcdBootStage = 1 and  Follow "Debug Lib Selection" to enable serial debug capability.
4. Audit all other PCD settings in the board DSC file to verify the values are correct for
your board.
5. Verify the flash layout is compliant with this specification.
6. Verify the required binaries will be included in the image produced in the build.
7. Verify the code execution path for Stage I will only perform the actions required to
achieve debug output.
8. Boot the system, collect the debug log, and verify the test point results defined in the
Test Point section are correct.

---?image=assets/images/slides/Slide_TableDHote.JPG
@title[Staged Approach by Features Section 02 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Staged Approach by Features</b>)</span><br><span style="font-size:0.75em;" >- Platform Firmware Boot Stage PCD</span></p>


@snap[north-west span-50 ]
<br>
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 1&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Enable Debug &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Stage 2&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Memory Initialization)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 3&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot to UEFI Shell only &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 4&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 5&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS w/ Security enabled&nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 6&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Advanced Feature Selection)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 7&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Performance Opetimizations &nbsp;)</span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south-east span-45 ]
<p style="line-height:50%" align="left" ><span style="font-size:0.6em;" >
PCD Is tested within .FDF to see which modules to include 
</span></p>
@snapend



@snap[south-east span-13 ]
<p style="line-height:20%" align="left" ><span style="font-size:02.1em;" >
2
<br><br>
</span></p>
<br><br>
@snapend

Note:
table d’hôte  
Image source: http://3.bp.blogspot.com/-nCzQh7Xu3_I/Uzk1a4DRk-I/AAAAAAAABCY/lQvT1cbn8Ug/s1600/5892-Caucasian-Man-Sitting-At-A-Table-And-Reading-A-Menu-At-A-Restaurant-Clipart-Illustration.jpg



Depending on the stage # provides some idea regarding what components are needed for a BIOS solution. It can be 3M full featured BIOS, or only 256K if just the basic boot is required, in some cases. 

This work can be done by defining some default configuration in PlatformConfig.dsc. 
For example, PcdBootStage|4 can be used to configure a BIOS to support a boot to OS (with ACPI/SMM), or PcdBootStage|3 to configure a BIOS to boot to shell only (without ACPI/SMM) 

- Stage I - Minimal Debug
  - Serial Port, Port 80, External debuggers Optional: Software debugger
- Stage II  - Memory Functional
  - Basic hardware initialization including main memory
- Stage III - Boot to UEFI Shell
   - Generic DXE driver execution
- Stage IV - Boot to OS
  - Boot a general purpose operating system with the minimally required feature set. Publish a minimal set of ACPI tables.- Stage V -Security Enabled
  - UEFI Secure Boot, TCG trusted boot, DMA protection, etc.
- Stage VI - Advanced Feature Selection
  - Firmware update, power management, networking support, manageability, testability, reliability, availability, serviceability, non-essential provisioning and resiliency mechanisms
- Stage VII – Tuning
   - Size and performance optimizations



---?image=assets/images/slides/Slide46.JPG
@title[Boot Flow – Stage 2]
<p align="right"><span class="gold" >@size[1.1em](<b>Boot Flow – Stage 2</b>)</span><span style="font-size:0.75em;" ></span></p>


Note:

 The objective of Stage II is to enable a minimal boot path memory initialization code execution that successfully installs permanent memory.



---?image=assets/images/slides/Slide47.JPG
@title[High Level Control Flow – Stage 2]
<p align="right"><span class="gold" >@size[1.1em](<b>High Level Control Flow – Stage 2</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-east span-58 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.85em; "><br>
Major Execution Activities
</span></p>

<ul style="list-style-type:disc; line-height:0.7;">
  <li><span style="font-size:0.65em" > Complete execution of the memory initialization module</span> </li>
  <li><span style="font-size:0.65em" > Discover, train and install permanent memory </span> </li>
  <li><span style="font-size:0.65em" > Migrate the temporary memory/stack to permanent memory.</span> </li>
  <li><span style="font-size:0.65em" > Migrate any code modules from temporary RAM to permanent memory.</span> </li>
  <li><span style="font-size:0.65em" > Perform cache configuration for a post-memory environment.</span> </li>
  <li><span style="font-size:0.65em" > Execute memory installed notification actions.</span> </li>
</ul>
@snapend

Note:

Stage II extends the Stage I control flow by executing the platform and silicon initialization required for memory initialization. The stage is completed when permanent memory is installed. Since execution prior to memory initialization typically occurs in a resource-constrained environment, the code in this stage is not compressed. To simplify silicon enabling which may be opaque to the board engineer in the form of a binary blob, Stage II enabling does not strictly constrain the extent of silicon initialization. In particular, it is recommended to perform standard security lock functionality such as register locks, privilege level changes, and other actions that are in the system requirements to reduce conditional logic and therefore potential for error in enabling those settings. This only pertains to security settings within the chipset. This does not include larger industry standard security features such as UEFI Secure Boot and TCG measured boot. Those features are enabled in Stage V Security Enable.

#### Stage II functionality:
- Non-volatile storage read-only access
- Pre-memory silicon policy initialization - Basic services like cache and CPU IO
- Initialization of decompression capability
- Memory initialization and basic memory test  


---
@title[Stage 2 Firmware Volumes]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 2 Firmware Volumes</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Name&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Content</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvPostMemory&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >Post-memory modules&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvFspM&nbsp;</span></p></td>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >Memory initialization</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;-&gt;FvPreMemorySilicon&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >Pre-memory silicon initialization&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvFspS&nbsp;</span></p></td>
		<td bgcolor="#323232" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >Silicon initialization</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;-&gt;FvPostMemorySilicon&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".0%2"><p style="line-height:01%"><span style="font-size:0.5em" >Post-memory silicon initialization &nbsp;</span></p></td>
	</tr>
</table>
<br>
@snapend



Note:

Stage II leverages most of the Stage I content.
Notice FvFspM is in both Stage 1 and stage 2




---
@title[Stage 2 FVs Contents]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 2 FVs Contents</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>FV&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Components</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Purpose</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvPostMemory&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >PlatformInitPostMem.efi&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".020%" width="70%"><p style="line-height:022%"><span style="font-size:0.45em" >Performs post memory initialization		&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >FspsWrapperPeim.efi &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" >Calls FSP-M & FSP-S FV </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > SiliconPolicyPeiPostMem.efi&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" >Publishes silicon initialization configuration </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > DxeIpl.efi&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" > Load and invoke DXE</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >. . . &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" > &nbsp;</span></p></td>
	</tr>

</table>
<br>
@snapend

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Mapped according to .FDF file layout<br><br>&nbsp;</span></p>)
@snapend


Note:

Main purpose is to initialize memory.
Example show Kabylake with FSP wrapper to call the FSP MemoryInit function inside FSP module.


---
@title[Stage 2 Platform Libraries - PEI]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 2 Platform Libraries - PEI</b>)</span><span style="font-size:0.75em;" ></b></span></p>


@snap[north-west span-100 ]
<br>
<br>
<table id="recTable-1">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Item</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>API Definition</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Producing Pkg</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Description</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > BoardInitLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > BoardPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:01%"><span style="font-size:0.4em" > Board initialization library. </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > SiliconPolicyInitLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > IntelSiliconPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > SiliconPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:020%"><span style="font-size:0.4em" > Provides default silicon configuration policy data. </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:020%"><span style="font-size:0.4em; font-family:Consolas;" > SiliconPolicy UpdateLib &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > IntelSiliconPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > BoardPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:020%"><span style="font-size:0.4em" >  Provides board updates to silicon configuration policy data.</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > TestPointCheckLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:020%"><span style="font-size:0.4em" >  Test point check library.</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > TestPointLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:020%"><span style="font-size:0.4em" >  Test point library.</span></p></td>
	</tr>
</table>
<br>
@snapend




Note:

BoardInitLib 
-  MinPlatformPkg - BoardPkg  - Board initialization library.
SiliconPolicyInitLib 
 - IntelSiliconPkg SiliconPkg Provides default silicon configuration policy data.
SiliconPolicyUpdateLib 
- IntelSiliconPkg BoardPkg Provides board updates to silicon configuration policy data.
TestPointCheckLib 
- MinPlatformPkg MinPlatformPkg Test point check library. It is called by PlatformInit module to perform stagespecific checks.
TestPointLib 
MinPlatformPkg MinPlatformPkg Test point library. It provides helper functionality for TestPointCheck lib.


---
@title[Stage 2 Platform Libraries - DXE]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 2 Platform Libraries - DXE</b>)</span><span style="font-size:0.75em;" ></b></span></p>


@snap[north-west span-100 ]
<br>
<br>
<table id="recTable-1">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Item</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>API Definition</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Producing Pkg</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Description</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  ResetSystemLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  MdeModulePkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  SiliconPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:01%"><span style="font-size:0.4em" >  For DXE reset architecture protocol</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  PciHostBridgeLib&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  MdeModulePkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  SiliconPkg&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:01%"><span style="font-size:0.4em" > For DXE PCI host bridge driver </span></p></td>
	</tr>
</table>
<br>
@snapend




Note:
Stage II contains some DXE items needed to enable Stage III. No board porting of these libraries is required. Board integrators should ensure that their silicon package provides the necessary libraries. These libraries and the UEFI Components (DXE) are functionally irrelevant to Stage II functionality.

ResetSystemLibSilicon/ Intel /KabylakeSiliconPkg/Pch/Library/DxeRuntimeResetSystemLib/DxeRuntimeResetSystemLib

PciHostBridgeLib

- Kabylake:
   - MinPlatformPkg/Pci/Library/PciHostBridgeLibSimple/PciHostBridgeLibSimple
  used in /MdeModulePkg/Bus/Pci/PciHostBridgeDxe/PciHostBridgeDxe



---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Modules - Stage 2 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Modules <br>- Stage 2</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-49 ]
<br>
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
MinPlatformPkg/<br>&nbsp;&nbsp;
  Include/<br>&nbsp;&nbsp;&nbsp;&nbsp;
     Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	   @color[yellow](BoardnitLib.h)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	   @color[yellow](SiliconPolicyInitLib.h)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	   @color[yellow](SiliconPolicyUpdateLib.h)<br>&nbsp;&nbsp;
  Library/<br>&nbsp;&nbsp;
  . . .<br>&nbsp;&nbsp;
  PlatformInit/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitPei/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PlatformInitPreMem/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	  PlatformInitPostMem/<br>&nbsp;&nbsp;
<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-46 ]
<br>
<br>
<br>
<p style="line-height:50%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
BoardBootModeDetect&lpar;&rpar;<br>
BoardInitBeforeMemoryInit&lpar;&rpar;<br>
<br>
MemoryInit&lpar;&rpar;<br>
<br>
SiliconPolicyInitPreMemory&lpar;&rpar;<br>
SiliconPolicyUpdatePreMemory&lpar;&rpar;<br>
SiliconPolicyDonePreMemory&lpar;&rpar;<br>
<br>&nbsp;&nbsp;
</span></p>
@snapend



Note:

The PlatformInit folder (Intel/MinPlatformPkg/PlatformInit) - PlatformInitPei, PlatformInitDxe and PlatformInitSmm control the platform initialization flow. Because this flow needs to involve the board initialization,  there is a set of  board hook points defined in BoardInitLib (MinPlatformPkg/Include/Library/BoardInitLib.h) 



---
@title[Platform Initialization Memory Init]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Memory Init</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-98 ]
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
<font color="gray">edk2-platforms/<br>&nbsp;
Platform/Intel/MinPlatformPkg/<br>&nbsp;&nbsp;
 . . .<br>&nbsp;&nbsp;
 PlatformInit/<br>&nbsp;&nbsp;&nbsp;
  PlatformInitPei/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;;&nbsp;
     PlatformInitPreMem.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     PlatformInitPostMem.c<br>
	 <br><br></font>
edk2/<br>&nbsp;&nbsp;
  FspIntelFsp2WrapperPkg/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    FspmWrapperPeim/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      @color[yellow](FspMemoryInitApi&lpar;&rpar;)
<br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-47 ]
<br><br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
<font face="Arial"> Notify call back </font><br>&nbsp;&nbsp;
  @color[yellow](BoardInitAfterMemoryInit&lpar;&rpar;)
</span></p>
@snapend

@snap[south-east span-40 fragment]
@box[bg-green-pp text-black waved my-box-pad2 ](<p style="line-height:70%" align="center"><span style="font-size:0.65em; font-family:Consolas;" >@size[1.3em](FSP-M)<br>&nbsp;<br> FspMemoryInitApi&lpar;&rpar;<br><br>&nbsp;</span></p>)
<br>
<br>
@snapend



Note:

Memory Initialization  done using the FSP Memory Init API through the FSP wrapper.


---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Modules]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Modules</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
MinPlatformPkg/<br>&nbsp;&nbsp;
 . . .<br>&nbsp;&nbsp;
 PlatformInit/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
  PlatformInitPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   @color[gray](PlatformInitPreMem)/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   @color[yellow](PlatformInitPostMem)/ <br>&nbsp;&nbsp;
 <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    @color[cyan](BoardInitBeforeSiliconInit&lpar;&rpar; )<br>&nbsp;&nbsp;
  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitEndOfPei() <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     BoardInitAfterSiliconInit() <br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-47 ]
<br><br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
KabylakeOpenBoardPkg/ <br>&nbsp;&nbsp;
 KabylakeRvp3/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
  Library/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   BoardInitLib/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     PeiKabylakeRvp3InitPostMemLib.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        @color[cyan](KabylakeRvp3)/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        @color[cyan](BoardInitBeforeSiliconInit&lpar;&rpar;) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
		  ConfigureGpio() <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
		    . . . <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
		  LateSiliconInit() <br>&nbsp;&nbsp;
<br>&nbsp;&nbsp;
</span></p>
@snapend


@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Hook for Before Silicon Initialization<br><br>&nbsp;</span></p>)
@snapend

Note:


From the Kabylake FDF PlatformInitPostMem module has 
 BoardInitBeforeSiliconInit()
    PlatformInitEndOfPei()
     BoardInitAfterSiliconInit()

And the Platform Libs to go with this are in edk2-platforms/Platform/Intel/
KabylakeOpenBoardPkg/KabylakeRvp3/Library/BoardInitLib/PeiKabylakeRvp3InitPostMemLib.c

With call to: KabylakeRvp3BoardInitBeforeSiliconInit()



---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Modules 02]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Modules</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
MinPlatformPkg/<br>&nbsp;&nbsp;
 . . .<br>&nbsp;&nbsp;
 PlatformInit/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
  PlatformInitPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   @color[gray](PlatformInitPreMem)/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   @color[yellow](PlatformInitPostMem)/ <br>&nbsp;&nbsp;
 <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    @color[gray](BoardInitBeforeSiliconInit&lpar;&rpar; )<br>&nbsp;&nbsp;
  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitEndOfPei() <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      @color[cyan](BoardInitAfterSiliconInit&lpar;&rpar; ) <br>&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-47 ]
<br><br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
KabylakeOpenBoardPkg/ <br>&nbsp;&nbsp;
 KabylakeRvp3/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
  Library/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   BoardInitLib/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     PeiBoardInitPostMemLib.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        @color[cyan](BoardInitAfterSiliconInit&lpar;&rpar;) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<br>&nbsp;&nbsp;
</span></p>
@snapend


@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Hook for After Silicon Initialization<br><br>&nbsp;</span></p>)
@snapend

Note:


Same but now for BoardInitAfterSilicon
From the Kabylake FDF PlatformInitPostMem module has 
 BoardInitBeforeSiliconInit()
    PlatformInitEndOfPei()
     BoardInitAfterSiliconInit()

And the Platform Libs to go with this are in edk2-platforms/Platform/Intel/
KabylakeOpenBoardPkg/KabylakeRvp3/Library/BoardInitLib/PeiBoardInitPostMemLib.c

For Kabylake just returns EFI_SUCCESS



---?image=assets/images/slides/Slide37.JPG
@title[FSP Wrapper for Silicon Initialization ]
<p align="right"><span class="gold" >@size[1.1em](<b>FSP Wrapper for Silicon Initialization </b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-98 ]
<br><br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
edk2/<br>&nbsp;&nbsp;
  FspIntelFsp2WrapperPkg/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    FspmWrapperPeim/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      @color[yellow](PeiMemoryDiscovredNotify&lpar;&rpar;)  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        <font face="Arial">Finish Memory Migration</font>   <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        <font face="Arial">--&gt;FSP Silcon Init API </font><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        @color[cyan](PostFspHobProcess&lpar;&rpar;)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-47 ]
<br><br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
MinPlatformPkg/FspWrapper/<br>&nbsp;&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;
   PeiFspWrapperHobProcessLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    FspWrapperHobProcessLib.c<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      @color[cyan](PostFspsHobProcess&lpar;&rpar;)
</span></p>
@snapend

@snap[south-east span-40 fragment]
@box[bg-green-pp text-black waved my-box-pad2 ](<p style="line-height:70%" align="center"><span style="font-size:0.65em; font-family:Consolas;" >@size[1.3em](FSP-S)<br>&nbsp;<br> FspSiliconInitApi&lpar;&rpar;<br><br>&nbsp;</span></p>)
<br>
<br>
@snapend



Note:

 FSP Wrapper is used to call into the FSP-S for the FspSiliconInit API.

---
@title[Silicon Policy Update Lib ]
<p align="right"><span class="gold" >@size[1.1em](<b>Silicon Policy Update Lib </b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-95 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.8em; ">
Using the <font face="Consolas">@color[yellow](SiliconPolicyUpdateLib)</font>, the board package may reference a variety of sources to obtain the board-specific policy values
</span></p>
<ul style="list-style-type:none; line-height:0.7;">
    <li><span style="font-size:0.7em" >1.&nbsp; PCD database  </span> </li>
    <li><span style="font-size:0.7em" >2.&nbsp; UEFI Variable </span> </li>
    <li><span style="font-size:0.7em" >3.&nbsp; Binary Blob </span> </li>
    <li><span style="font-size:0.7em" >4.&nbsp; Built-in C structure </span> </li>
    <li><span style="font-size:0.7em" >5.&nbsp; Hardware information </span> </li>
</ul>
@snapend




@snap[east span-24 ]
<br><br>
![SiliconPolicyLib](/assets/images/SiliconPolicyLib.png)
@snapend



@snap[south span-100 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">One silicon policy data structure created per silicon module<br><br>&nbsp;</span></p>)
<br>
@snapend


Note:

One silicon policy data structure is created per silicon module. The data structure should
only contain data. Functions should not be used in silicon policy data.
When a silicon module installs this policy data, it should consider the most common usage
as the default policy data. Therefore, a board module must only update non-default values
instead of all fields.

http://infodome.wikidot.com/local--files/rules-of-combat-dome/rule_book1.gif


---
@title[Silicon Policy APIs ]
<p align="right"><span class="gold" >@size[1.1em](<b>Silicon Policy APIs </b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-75 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.9em; ">
Silicon code exposes  APIs to:
</span></p>
<ul style="list-style-type:disc; line-height:0.75;">
    <li><span style="font-size:0.8em" > Initialize all policy data to the default value, based upon the current silicon. </span> </li>
    <li><span style="font-size:0.8em" > Inform silicon code that all policy data have been updated, and they are ready to consume. </span> </li>
</ul>
@snapend




@snap[east span-24 ]
<br><br>
![API_Pic](/assets/images/API_Pic.png)
@snapend



@snap[south span-100 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Board module only updates non-default values<br><br>&nbsp;</span></p>)
<br>
@snapend


Note:

http://mathinsight.org/media/image/image/function_machine.png

This silicon code may expose the APIs:
An API to initialize all policy data to the default value, based upon the current silicon.
An API to tell silicon code that all policy data have been updated, and they are ready to consume.

a board module must only update non-default values
instead of all fields.








---?image=assets/images/slides/Slide58.JPG
@title[FSP Silicon Policy Data Flow ]
<p align="right"><span class="gold" >@size[1.1em](<b>FSP Silicon Policy Data Flow</b>)</span><span style="font-size:0.75em;" ></span></p>



Note:
Slide from: https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification 4.6.1.5 Intel® FSP Policy Data Flow


After policy configuration is completed, the board may indicate that the policy is configured
with board-specific actions in the SiliconPolicyDonePreMemory ( ) API in SiliconPolicyInitLib

<pre>
UpdateFspmUpdData (Upd)
SiliconPolicyInitPreMemory ()
SiliconPolicyUpdatePreMemory ()
Minimum platform: Minor update of relevant options
Fully featured platform (Stage VI and greater): Full update for all platform features
SiliconPolicyDonePreMemory ()
</pre>




---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Silicon]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Silicon</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
MinPlatformPkg/ <br>&nbsp;&nbsp;
  . . . <br>&nbsp;&nbsp;
  PlatformInit/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
 <br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiliconPolicyPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       SiliconPolicyPeiPostMem.c <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         SiliconPolicyPeiPostMemEntrypoint() <br> <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[cyan](SiliconPolicyInitPostMem &lpar;&rpar;)  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[yellow](SiliconPolicyUpdatePostMem&lpar;&rpar;) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[yellow](SiliconPolicyDonePostMem&lpar;&rpar;) 
</span></p>
@snapend

@snap[north-east span-47 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Silicon/Intel/<br>
KabylakeSiliconPkg/<br>&nbsp;&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    PeiSiliconPolicyInitLibFsp/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PeiFspPolicyInitLib.c <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        @color[cyan](SiliconPolicyInitPostMem&lpar;&rpar;) <br><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        <font face="Arial">// Using the FSP Update policy  </font> <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          @color[yellow](PeiFspPchPolicyInit &lpar;&rpar;) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          @color[yellow](PeiFspMePolicyInit &lpar;&rpar;) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          @color[yellow](PeiFspSaPolicyInit &lpar;&rpar;) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          @color[yellow](PeiFspCpuPolicyInit &lpar;&rpar;) 
</span></p>
@snapend





@snap[south span-100 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Example: Kabylake - post-mem FSP Silicon Init<br><br>&nbsp;</span></p>)
@snapend


Note:

Kabylake example:
Slide show location of the Platform vs. silicon modules corresponding to the Silicon Policy updates after memory init. 

Platform calls silicon module relying on the FSP code to manage the underling data structures.


---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Silicon 02]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Silicon</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
MinPlatformPkg/ <br>&nbsp;&nbsp;
  . . . <br>&nbsp;&nbsp;
  PlatformInit/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
 <br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiliconPolicyPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       SiliconPolicyPeiPostMem.c <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         SiliconPolicyPeiPostMemEntrypoint() <br> <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[gray](SiliconPolicyInitPostMem &lpar;&rpar;)  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[cyan](SiliconPolicyUpdatePostMem&lpar;&rpar;) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[yellow](SiliconPolicyDonePostMem&lpar;&rpar;) 
</span></p>
@snapend

@snap[north-east span-47 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
KabylakeOpenBoardPkg/<br>&nbsp;&nbsp;
  FspWrapper/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PeiSiliconPolicyUpdateLibFsp/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        PeiFspPolicyUpdateLib.c <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          @color[cyan](SiliconPolicyUpdatePostMem&lpar;&rpar;) <br><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          @color[yellow](PeiFspSaPolicyUpdate &lpar;&rpar;)        <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          @color[yellow](PeiFspPchPolicyUpdate &lpar;&rpar;) 
</span></p>
@snapend





@snap[south span-100 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Notice the Update is from board FSP Wrapper Library<br><br>&nbsp;</span></p>)
@snapend


Note:

Notice the Update Post mem is from the Kabylake FSP wrapper and not the silicon.

This is because the previous slide (init) already  got the FSP API pointer so the board can now just do the update.


Performs silicon post-mem policy update.

  The meaning of Policy is defined by silicon code.
  It could be the raw data, a handle, a PPI, etc.
  
  The input Policy must be returned by SiliconPolicyDonePostMem().
  
  1) In FSP path, the input Policy should be FspsUpd.
  A platform may use this API to update the FSPS UPD policy initialized
  by the silicon module or the default UPD data.
  The output of FSPS UPD data from this API is the final UPD data.


---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Silicon 03]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Silicon</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-49 ]
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
MinPlatformPkg/ <br>&nbsp;&nbsp;
  . . . <br>&nbsp;&nbsp;
  PlatformInit/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
 <br>&nbsp;&nbsp;&nbsp;&nbsp;
    SiliconPolicyPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       SiliconPolicyPeiPostMem.c <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         SiliconPolicyPeiPostMemEntrypoint() <br> <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[gray](SiliconPolicyInitPostMem &lpar;&rpar;)  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[gray](SiliconPolicyUpdatePostMem&lpar;&rpar;) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[cyan](SiliconPolicyDonePostMem&lpar;&rpar;) 
</span></p>
@snapend

@snap[north-east span-47 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Silicon/Intel/<br>
KabylakeSiliconPkg/<br>&nbsp;&nbsp;
  Library/<br>&nbsp;&nbsp;&nbsp;&nbsp;
    PeiSiliconPolicyInitLibFsp/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      PeiFspPolicyInitLib.c <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        @color[cyan](SiliconPolicyDonePostMem&lpar;&rpar;) <br><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 </span></p>
@snapend




@snap[south span-100 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Silicon post-mem policy is finalized<br><br>&nbsp;</span></p>)
@snapend


Note:

The silicon post-mem policy is finalized.
  Silicon code can do initialization based upon the policy data.

  The input Policy must be returned by SiliconPolicyInitPostMem().
 
---
@title[Prepare for Hand-off to DXE]
<p align="right"><span class="gold" >@size[1.1em](<b>Prepare for Hand-off to DXE</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-east span-70 ]

<p style="line-height:20%" align="left" ><span style="font-size:0.7em;" ><br><br><br>&nbsp;</span></p>
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:70%"><span style="font-size:0.8em;" ><b>&nbsp;</b><br><br><br>&nbsp;</span></p>)
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:70%"><span style="font-size:0.8em;" ><b>&nbsp;</b><br><br><br>&nbsp;</span></p>)
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:70%"><span style="font-size:0.8em;" ><b>&nbsp;</b><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-west span-31 ]
<p style="line-height:20%" align="left" ><span style="font-size:0.7em;" ><br><br><br>&nbsp;</span></p>
@box[bg-royal text-white rounded my-box-pad2  ](<p style="line-height:70%"><span style="font-size:0.8em;" ><br><b>Hob Output</b><br><br>&nbsp;</span></p>)
@box[bg-royal text-white rounded my-box-pad2  ](<p style="line-height:70%"><span style="font-size:0.8em;" ><b>MTRR <br>Configuration</b><br><br>&nbsp;</span></p>)
@box[bg-royal text-white rounded my-box-pad2  ](<p style="line-height:70%"><span style="font-size:0.8em;" ><br><b>DXE IPL</b><br><br>&nbsp;</span></p>)
@snapend



@snap[north-east span-67 ]
<p style="line-height:20%" align="left" ><span style="font-size:0.7em;" ><br><br><br><br><br><br>&nbsp;</span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.67em;" >&bull; 2 Hob lists - FSP &  FSP Wrapper<br><br><br><br></span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.67em;" >&bull; 2 locations – after permanent Memory & Prior to <br>&nbsp;&nbsp;&nbsp; DXE IPL platform's capabilities <br><br><br><br> </span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.67em;" >&bull; Load and invoke DXE <br><br><br><br> </span></p>

@snapend


Note:

Intel® FSP HOB to PEI HOB transition


In an Intel® FSP API mode boot with an EDK II wrapper, the system will have two HOB
lists - one maintained in the FSP PEI environment and the other in the FSP wrapper PEI
environment. The FSP wrapper environment is responsible for converting data from the
FSP HOB to a PEI HOB. These HOBs are platform-specific; examples include the
SmbiosHob and GraphicInfoHob.


MTRR Configuration Settings in Post-Memory
The system MTRR settings are typically configured in two locations after permanent memory
initialization.


1. After permanent memory installation


At this point, cache attributes are set for PEI memory usage. This specification does not
require any particular MTRR configuration, as it is ultimately dependent upon platform
goals such as functionality and performance given the device and storage technologies
present on the platform. The most common ranges configured are the default memory
setting as UC, the DRAM region as WB, and the SPI flash MMIO region as WP. These
settings are usually applied in a memory installation notification function or a PEIM
shadow. The architecture requires that the settings be applied in the board package.


2. Prior to DXE IPL


At this point PEI execution has completed and control is transitioning to the DXE phase.
The MTRR settings are typically modified to prepare for the DXE environment. The
most common ranges configured are the default memory as WB, the TSEG (SMRAM)
region as UC, and MMIO as UC. These settings are usually applied in an end of PEI
notification function. The architecture requires that the settings be applied in the board
package.



---
@title[Stage 2 Checklist  ]
<p align="center"><span class="gold" >@size[1.1em](<b>Stage 2 Checklist</b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; ">
Steps to enable a board for Stage 2.
</span></p>

@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

@snap[north-east span-98 ]
<br>
<br>
<br>
<ul style="list-style-type:None; line-height:0.7;">
  <li><span style="font-size:0.65em" >1. Update <font face="Consolas"><i>@color[cyan](NewOpenBoardPkg/BoardXxx) </i></font></span> </li>
  <ul style="list-style-type:disc; line-height:0.6;">
      <li><span style="font-size:0.55em" > Add Board boot mode detection code in BoardBootModeDetect () , <font face="Consolas">@color[yellow](BoardXxx/BoardInitLib/PeiBoardXxxInitPreMemoryLib.c.)</font> </span> </li>
      <ul style="list-style-type:none; line-height:0.5;">
        <li><span style="font-size:0.5em" > - The boot mode can be hardcoded. It should reflect actual functionality based upon<br>&nbsp;&nbsp;&nbsp;
             the feature, such as S3 (silicon register), Capsule (variable), Recovery(GPIO). </span> </li>
      </ul>
      <li><span style="font-size:0.55em" > Add Board pre-memory initialization code in <font face="Consolas">@color[yellow](BoardInitBeforeMemoryInit &lpar;&rpar;) and @color[yellow](BoardInitAfterMemoryInit &lpar;&rpar; , BoardXxx/BoardInitLib/PeiBoardXxxInitPreMemLib.c.)</font> </span> </li>
      <ul style="list-style-type:none; line-height:0.5;">
        <li><span style="font-size:0.5em" > - It initializes board specific hardware devices, such as GPIO.</span> </li>
        <li><span style="font-size:0.5em" > - It also updates pre-memory policy configuration by using PCD </span> </li>
      </ul>
      <li><span style="font-size:0.55em" > Add Board policy update code in <font face="Consolas">@color[yellow](SiliconPolicyUpdatePreMemory &lpar;&rpar; , BoardXxx/PeiSiliconPolicyUpdateLib/PeiBoardXxxInitPreMemoryLib.)</font> </span> </li>
      <ul style="list-style-type:none; line-height:0.5;">
        <li><span style="font-size:0.5em" > - The PCD updated in <font face="Consolas">@color[yellow](BoardInitBeforeMemoryInit &lpar;&rpar; ) </font>might be used here. </span> </li>
      </ul>
  </ul>
  <li><span style="font-size:0.65em" >2.  Ensure all PCDs in the configuration section (DSC files) are correct for your 
    <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;board. </span> </li>
  <li><span style="font-size:0.65em" >3.  Ensure all required binaries in the flash file (FDF files) are correct for your 
    <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;board .</span> </li>
 
  <li><span style="font-size:0.65em" >4. Boot, collect log, verify test point results are correct.  </span> </li>
 
</ul>
<p style="line-height:70%" align="left" ><span style="font-size:0.45em; ">
<a href="https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/4_stage_2_memory_functional/49_test_point_results.html">EDK II Open Platform Spec Test points Stage 2</a>
</span></p>

@snapend


Note:

Steps to enable a board for Stage II
1.  Update the NewOpenBoardPkg/BoardXxx
  i. Add Board boot mode detection code in BoardBootModeDetect () ,    BoardXxx/BoardInitLib/PeiBoardXxxInitPreMemoryLib.c.
     i. The boot mode can be hardcoded. It should reflect actual functionality based upon the feature, such as S3 (silicon register), Capsule (variable), Recovery (GPIO).
  ii. Add Board pre-memory initialization code in BoardInitBeforeMemoryInit () and BoardInitAfterMemoryInit () , BoardXxx/BoardInitLib/PeiBoardXxxInitPreMemLib.c.
  i. It initializes board specific hardware devices, such as GPIO.
  ii. It also updates pre-memory policy configuration by using PCD
  iii. Add Board policy update code in SiliconPolicyUpdatePreMemory () ,

BoardXxx/PeiSiliconPolicyUpdateLib/PeiBoardXxxInitPreMemoryLib.c.
  i. The PCD updated in BoardInitBeforeMemoryInit () might be used here.
2. Ensure all PCDs in the configuration section (DSC files) are correct for your board.
  i. Set gMinPlatformPkgTokenSpaceGuid.PcdBootStage = 2
3. Ensure all required binaries in the flash file (FDF files) are correct for your board.
4. Boot, collect log, verify test point results defined in section 4.9 from the EDK II Open Platform spec are correct.



---?image=assets/images/slides/Slide_TableDHote.JPG
@title[Staged Approach by Features Section 03 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Staged Approach by Features</b>)</span><br><span style="font-size:0.75em;" >- Platform Firmware Boot Stage PCD</span></p>


@snap[north-west span-50 ]
<br>
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 1&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Enable Debug &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 2&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Memory Initialization)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Stage 3&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Boot to UEFI Shell only &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 4&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 5&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS w/ Security enabled&nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 6&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Advanced Feature Selection)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 7&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Performance Opetimizations &nbsp;)</span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south-east span-45 ]
<p style="line-height:50%" align="left" ><span style="font-size:0.6em;" >
PCD Is tested within .FDF to see which modules to include 
</span></p>
@snapend


@snap[south-east span-13 ]
<p style="line-height:20%" align="left" ><span style="font-size:02.1em;" >
3
<br><br>
</span></p>
<br><br>
@snapend


Note:
table d’hôte  
Image source: http://3.bp.blogspot.com/-nCzQh7Xu3_I/Uzk1a4DRk-I/AAAAAAAABCY/lQvT1cbn8Ug/s1600/5892-Caucasian-Man-Sitting-At-A-Table-And-Reading-A-Menu-At-A-Restaurant-Clipart-Illustration.jpg



Depending on the stage # provides some idea regarding what components are needed for a BIOS solution. It can be 3M full featured BIOS, or only 256K if just the basic boot is required, in some cases. 

This work can be done by defining some default configuration in PlatformConfig.dsc. 
For example, PcdBootStage|4 can be used to configure a BIOS to support a boot to OS (with ACPI/SMM), or PcdBootStage|3 to configure a BIOS to boot to shell only (without ACPI/SMM) 

- Stage I - Minimal Debug
  - Serial Port, Port 80, External debuggers Optional: Software debugger
- Stage II  - Memory Functional
  - Basic hardware initialization including main memory
- Stage III - Boot to UEFI Shell
   - Generic DXE driver execution
- Stage IV - Boot to OS
  - Boot a general purpose operating system with the minimally required feature set. Publish a minimal set of ACPI tables.- Stage V -Security Enabled
  - UEFI Secure Boot, TCG trusted boot, DMA protection, etc.
- Stage VI - Advanced Feature Selection
  - Firmware update, power management, networking support, manageability, testability, reliability, availability, serviceability, non-essential provisioning and resiliency mechanisms
- Stage VII – Tuning
   - Size and performance optimizations



---?image=assets/images/slides/Slide65.JPG
@title[Boot Flow – Stage 3]
<p align="right"><span class="gold" >@size[1.1em](<b>Boot Flow – Stage 3</b>)</span><span style="font-size:0.75em;" ></span></p>


Note:

 The objective of Stage III is to enable a minimal boot path that successfully loads
the UEFI Shell. A secondary objective for Stage III is to be silicon and board agnostic. All
silicon and board specific details should be leveraged from Stages I and II. Demonstrating
the capability to load the UEFI shell does not imply that the UEFI shell is a required
component in the end product firmware. It does ensure that the platforms with a terminal
boot stage target greater than Stage II can load the UEFI shell so the system can be
analyzed and configured in the UEFI boot services environment with well-defined behavior in
a consistent manner with other Minimum Platform specification-compliant systems.

The minimal UI capability that is required is serial console. UEFI variables must be
supported with at least emulated variable behavior. UEFI variable storage to a non-volatile
media such as SPI NOR flash is acceptable if the platform requirements mandate such
support. Additional capabilities are optional and must not be assumed. These include USB
input devices, graphics devices, and other storage devices.





---?image=assets/images/slides/Slide66.JPG
@title[High Level Control Flow – Stage 3]
<p align="right"><span class="gold" >@size[1.1em](<b>High Level Control Flow – Stage 3</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-east span-60 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.85em; "><br>
Major Execution Activities
</span></p>

<ul style="list-style-type:disc; line-height:0.7;">
  <li><span style="font-size:0.65em" > DXE Initial Program Load (IPL) </span> </li>
  <li><span style="font-size:0.65em" > DXE Core initialization and dispatcher execution </span> </li>
  <li><span style="font-size:0.65em" > Initialize the generic infrastructure required for the DXE environment </span> </li>
  <ul style="list-style-type:none; line-height:0.6;">  
      <li><span style="font-size:0.6em" > -  DXE architectural protocols - Initialization of architecturally required hardware such as timers</span> </li>
  </ul>  
  <li><span style="font-size:0.65em" > Post-memory silicon policy initialization </span> </li>
  <li><span style="font-size:0.65em" > Serial console input and output capabilities</span> </li>
</ul>
@snapend

Note:

Stage III extends Stage II control flow by executing Driver Execution Environment (DXE),
executing Boot Device Selection (BDS) and invoking the UEFI Shell.

After memory is installed during Stage II, the remaining silicon and platform initialization
must take place in the PEI phase only. All silicon initialization tasks should have been
completed in Stage II, and there should be no silicon-specific initialization required in the
DXE phase. The default console information should be transferred via a HOB and initialized
and used in Stage III.

- Universally usable infrastructure: DXE Core, Minimal BDS, console infrastructure
- Silicon agnostic architectural protocol producing hardware modules
- UEFI Variable support (emulation allowed)
- UEFI Shell
- Tests for Memory Map, Cache Map, architectural hardware




---
@title[Stage 3 Firmware Volumes]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 3 Firmware Volumes</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Name&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Content</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvUefiBoot&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" >Common UEFI, DXE & BDS Services&nbsp;</span></p></td>
	</tr>
</table>
<br>
@snapend



@snap[north-west span-100 fragment]
<br>
<br>
<br>
<br>
<br>
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 3 FVs Contents</b>)</span><span style="font-size:0.75em;" ></span></p>

<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>FV&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Components</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Purpose</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >FvUefiBoot&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >DxeCore.efi&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".020%" width="70%"><p style="line-height:022%"><span style="font-size:0.45em" >UEFI Sytem table, DXE Services, Dispatcher & APs		&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > . . .  &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.45em" >All other UEFI / DXE Modules, See .FDF file</span></p></td>
	</tr>
</table>	
@snapend

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Mapped according to .FDF file layout<br><br>&nbsp;</span></p>)
@snapend


Note:

Stage III finalizes silicon and prepares DXE/BDS services
See 

https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/5_stage_3_boot_to_uefi_shell/52_firmware_volumes.html#52-firmware-volumes

for a list of more Modules in the FV for stage 3



---
@title[Stage 3 Platform Libraries - PEI]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 3 Platform Architecture Libraries</b>)</span><span style="font-size:0.75em;" ></b></span></p>


@snap[north-west span-100 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.75em;">
Stage 3 Modules - @size[.8em](List of UEFI and DXE Components: <a href="https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/content/appendix_a_full_maps/a1_firmware_volume_layout.html">EDK II Open Platform Spec.</a>)
<br>
<br>
<br>
<br>
Stage 3 Platform Architecture Libraries
</span></p>


<table id="recTable-1">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Item</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:30%"><span style="font-size:0.5em" ><b>API Definition</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:30%"><span style="font-size:0.5em" ><b>Producing Pkg</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Description</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > SerialPortLib </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MdeModulePkg </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg </span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:01%"><span style="font-size:0.4em" >  Serial port leveraging PEI and HOB initializatio </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > PlatformBootManagerLib </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MdeModulePkg </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > MinPlatformPkg </span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:01%"><span style="font-size:0.4em" >  Basic platform boot manager port. </span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south span-95 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Only modules in the board package should be modified <br><br>&nbsp;</span></p>)
@snapend


Note:



Only modules in the board package should be modified in the process of board porting. The minimum platform package and other common package 
contents must not be directly modified. The board package and silicon package modules may have multiple instances to support different boards and different silicon. 
These components are required. They enable orderly board porting and add the support for extensibility in later stages. The libraries consumed are the subset of 
libraries required by this specification. 

See:
https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/5_stage_3_boot_to_uefi_shell/53_modules.html#53-modules


To find the Libraries for the Platform specific code
1 Search the Work space .DSC files for the string of the library
2 Open the .DSC files associated with the platform
3 Determine which Library is used and that should have the build path in the workspace.


For KabyLake only the PlatformBootManagerLib will be ported.
Serial port is standard EDK II from MdeModulePkg/Library/BaseSerialPortLib16550



---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Modules - Stage 3 PEI]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Modules</b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:45%" align="left" ><span style="font-size:0.75em;">Silicon Initilization done in Stage 2 for Stage 3</span></p>

@snap[north-west span-49 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-49 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
MinPlatformPkg/ <br>&nbsp;&nbsp;
 Include/  <br>&nbsp;&nbsp;&nbsp;&nbsp;
  Library/  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   @color[yellow](BoardinitLib.h)  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   @color[yellow](SiliconPolicyInitLib.h)  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   @color[yellow](SiliconPolicyUpdateLib.h)  <br>&nbsp;&nbsp;
 <br>&nbsp;&nbsp;
 Library/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
  . . . <br>&nbsp;&nbsp;&nbsp;&nbsp;
  PlatformInit/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     PlatformInitPostMem/ 
</span></p>
@snapend

@snap[north-east span-45 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
BoardInitBeforeSiliconInit() <br>
 <br>
SiliconPolicyInitPostemory() <br>
SiliconPolicyUpdatePostMemory() <br>
SiliconPolicyDonePostMemory() <br>
 <br>
BoardInitAfterSiliconInit() <br>
 <br>
DxeLoadCore()
</span></p>

@snapend



@snap[south-east span-48 fragment]
<ul style="list-style-type:disc; line-height:0.7;">
  <li><span style="font-size:0.65em" > No silicon-specific initialization in DXE phase </span> </li>
  <li><span style="font-size:0.65em" > HOBs should transfer Init settings to Stage 3</span> </li>
</ul>
<br>
<br>
<br>
@snapend


Note:


The following functions on Right are required to exist and to execute in the listed order. The
component that provides the function is not specified because it is not required by the
architecture.

After memory is installed during Stage II, the remaining silicon and platform initialization
must take place in the PEI phase only. All silicon initialization tasks should have been
completed in Stage II, and there should be no silicon-specific initialization required in the
DXE phase. The default console information should be transferred via a HOB and initialized
and used in Stage III.




---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Modules - Stage 3 DXE]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Modules</b>)</span><span style="font-size:0.75em;" ><br>- Stage 3 DXE</span></p>

@snap[north-west span-49 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-49 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
MinPlatformPkg/ <br>&nbsp;&nbsp;
 Include/  <br>&nbsp;&nbsp;&nbsp;&nbsp;
  Library/  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
   @color[yellow](BoardinitLib.h)  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

 <br>&nbsp;&nbsp;
 Library/ <br>&nbsp;&nbsp;&nbsp;&nbsp;
  . . . <br>&nbsp;&nbsp;&nbsp;&nbsp;
  PlatformInit/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitPei/ <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     PlatformInitPostMem/ 
</span></p>
@snapend

@snap[north-east span-45 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.5em; font-family:Consolas;"><br>
BoardNotificationInit() <br>
 <br>
</span></p>

@snapend



@snap[south-east span-48 fragment]
<p style="line-height:70%" align="left" ><span style="font-size:0.75em" >
Create Events:<br>
&bull; &nbsp;&nbsp; PCI Enumeration complete<br>
&bull; &nbsp;&nbsp; DXE SMM ready to Lock
</span></p>
<br>
<br>
<br>
<br>
<br>
@snapend


Note:

BoardInitLib BoardNotificationInit Platform Board specific initialization hook
at DXE phase



---?image=assets/images/slides/Slide71.JPG
@title[Initial Program Load (IPL) PEIM for DXE]
<p align="right"><span class="gold" >@size[1.1em](<b>Initial Program Load (IPL) PEIM for DXE</b>)</span><span style="font-size:0.75em;" ></span></p>
<br>
<div class="left">
<span style="font-size:0.8em" > &nbsp;</span>
</div>
<div class="right">
<br>
@ul[no-bullet]
-  <font color="white">&nbsp;&nbsp;<b><font face="Consolas">DxeLoadCore&lpar;&rpar;</font> </b></font>  <BR><br>
-  <font color="#FFFF00">&nbsp;&nbsp;<b>Creates HOBs </b></font> <br><br>
-  <font color="white">&nbsp;&nbsp;<b>Locates DXE main </b></font>  <BR><br>
-  <font color="#ffc000">&nbsp;&nbsp;<b>Switch Stacks</b></font>  <br><br>
-  <font color="cyan">&nbsp;&nbsp;<b>&rarr;&nbsp;<font face="Consolas">DxeMain&lpar;&rpar;</font></b></font> 
@ulend
</div>			


Note:
-  The DXE IPL PEIM should not require porting, but  knowing what is does it important.  This is a good place for a breakpoint and starting to debug.  For example, if porting didn’t work this is where it will fail.

-  The DXE IPL PEIM performs several tasks

  -  Shadows DXE IPL into permanent memory to allow sharing of the decompression algorithm and several other library routines (e.g. security)
  -  Allocates 128KB of stack for the DXE phase
  -  Creates HOBs for passing library routines and the firmware volumes discovered during the PEI phase. Most commonly this is the main FV and any other FVs that DXE will use to load drivers from (for example backup block)
  -  If S3, then the OS waking vector is called
  -  Locate DXE Main in the FVs
  -  If not S3 then switch stacks and call DXE Main


Characteristics 
-  The last PEIM to execute
-  Shadows into permanent memory
-  Shares data from PEI phase with DXE
-  Creates a stack for DXE Phase
-  Creates HOBs
-  Calls S3 vector if appropriate
-  Locate DXE Main
-  Switch stack and call DXE Main





---?image=assets/images/slides/Slide72.JPG
@title[DXE Phase Stage 3]
<p align="right"><span class="gold" >@size[1.1em](<b>DXE Phase Stage 3</b>)</span><span style="font-size:0.75em;" ></span></p>

<div class="left-1">
<span style="font-size:0.8em" > &nbsp;</span>
</div>
<div class="right-1">
<br>
<br>
<ul style="list-style-type:none; line-height:0.8;">
  <li><span style="font-size:0.9em" ><font color="yellow">DXE Core initialization and dispatcher execution </font> </span></li><br>
  <li><span style="font-size:0.9em" ><font color="cyan">Establish Architectural Protocols </font> </span></li><br>
  <li><span style="font-size:0.9em" ><font color="#ffc000">Install any required DXE / UEFI Drivers for Stage 3 </font> </span></li>
</ul>
</div>		

Note:


Again, the DXE Main core code should not require porting, but  knowing what is does it important.

-  The main platform DXE code is in subdirectories of the platform package having “DXE” in the directory name (i.e. PciPlatformDxe)
   -  It will reference other packages DXE modules
-  Establish the architectural protocols
  -  Isolate platform specific hardware (e.g., RTC)
  -  Provide support for boot and runtime services
  -  Low level protocols that support DXE APIs
  -  Directly called by DXE core
-  Install any required DXE and then the UEFI Drivers


---?image=assets/images/slides/Slide73.JPG
@title[Architectural Protocols for KabyLake]
<p align="right"><span class="gold" >@size[1.1em](<b>Architectural Protocols for KabyLake</b>)</span><span style="font-size:0.75em;" ></span></p>

Note:


Silicon agnostic architectural protocol producing hardware modules

Example show KabyLake APs

For the gEfiTimerArchProtocolGuid 

Search the workspace for all .inf files with the string: gEfiTimerArchProtocolGuid 
Notice there are 2 where this protocol is gEfiTimerArchProtocolGuid                     ## PRODUCES
Next search the board/platform .dsc file for which .inf file is included.

We find that  PcAtChipsetPkg/HpetTimerDxe/HpetTimerDxe.inf is included in the platform .dsc file


- gEfiBdsArchProtocolGuid 	`MdeModulePkg/Universal/BdsDxe/ `
- gEfiCapsuleArchProtocolGuid 	`MdeModulePkg/Universal/CapsuleRuntimeDxe `
- gEfiCpuArchProtocolGuid                       	`UefiCpuPkg/CpuDxe/`
- gEfiMetronomeArchProtocolGuid 	`MdeModulePkg/Universal/Metronome`
- gEfiMonotonicCounterArchProtocolGuid 	`MdeModulePkg/Universal/MonotonicCounterRuntimeDxe `
- gEfiRealTimeClockArchProtocolGuid 	`PcAtChipsetPkg/PcatRealTimeClockRuntimeDxe`
- gEfiResetArchProtocolGuid 	`MdeModulePkg/Universal/ResetSystemRuntimeDxe`
- gEfiRuntimeArchProtocolGuid 	`MdeModulePkg/Core/RuntimeDxe `
- gEfiSecurity2ArchProtocolGuid 	`MdeModulePkg/Universal/SecurityStubDxe`
- gEfiStatusCodeRuntimeProtocolGuid 	`MdeModulePkg/Universal/ReportStatusCodeRouter/RuntimeDxe` 
- gEfiTimerArchProtocolGuid 	`PcAtChipsetPkg/HpetTimerDxe`
- gEfiVariableArchProtocolGuid 	`MdeModulePkg/Universal/Variable/RuntimeDxe/VariableRuntimeDxe` or        `VariableSmmRuntimeDxe` (depends on PcdBootToShellOnly)

- gEfiVariableWriteArchProtocolGuid 	`MdeModulePkg/Universal/Variable/RuntimeDxe/VariableRuntimeDxe` or   `VariableSmmRuntimeDxe` (depends on PcdBootToShellOnly)

- gEfiWatchdogTimerArchProtocolGuid 	`MdeModulePkg/Universal/WatchdogTimerDxe `




---?image=assets/images/slides/Slide37.JPG
@title[Platform Initialization Board Hook Modules - Stage 3 DXE]
<p align="right"><span class="gold" >@size[1.1em](<b>Platform Initialization Board Hook Modules</b>)</span><span style="font-size:0.75em;" ><br>- Stage 3 DXE - BDS</span></p>

@snap[north-west span-52 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-47 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
MinPlatformPkg/ <br>&nbsp;&nbsp;
 Bds/  <br>&nbsp;&nbsp;&nbsp;&nbsp;
  Library/  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      DxePlatformBootManagerLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         BdsPlatform/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
           @color[yellow](PlatformBootManagerBeforeConsole&lpar;&rpar;)
</span></p>
@snapend

@snap[north-east span-44 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.65em; font-family:Consolas;"><br><br>
PlatformBootManagerLib <br>
 <br>
</span></p>

@snapend



@snap[south-east span-95 ]
<p style="line-height:80%" align="left" ><span style="font-size:0.8em" >
&bull; &nbsp;&nbsp;Call before BDS to connect all devices<br>
&bull; &nbsp;&nbsp;Creates event,<font face="Consolas">@size[.8em](OnReadyToBootCallBack)</font><br>
&bull; &nbsp;&nbsp;Updates consule etc.<br>
</span></p>
<br>
<br>
@snapend



@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Typically, no board porting is required<br><br>&nbsp;</span></p>)
@snapend


Note:

To find the Libraries for the Platform specific code
1 Search the Work space .DSC files for the string of the library
2 Open the .DSC files associated with the platform
3 Determine which Library is used and that should have the build path in the workspace.

- Call before BDS to connect all devices
- Creates event, OnReadyToBootCallBack
- Updates consule etc.


- No board porting of these libraries is required.



---
@title[Stage 3 Checklist  ]
<p align="center"><span class="gold" >@size[1.1em](<b>Stage 3 Checklist</b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; ">
Steps to enable a board for Stage 3.
</span></p>

@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

@snap[north-west span-100 ]
<br>
<br>
<br>
<ul style="list-style-type:None; line-height:0.7;">
 <li><span style="font-size:0.65em" >1.&nbsp;&nbsp; Add board post-memory initialization code in 
 <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font face="Consolas">@size[.7em](BoardInitBeforeSiliconInit &lpar;&rpar;)</font> and <font face="Consolas">@size[.7em](BoardInitAfterSiliconInit &lpar;&rpar;)</font> ,
 <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font face="Consolas">@size[.7em](BoardPkg/BoardInitLib/PeiBoardXxxInitPostMemoryLib.c)</font></span> </li>
  <ul style="list-style-type:none; line-height:0.5;">
     <li><span style="font-size:0.5em" >&bull; &nbsp;&nbsp; Initialize board-specific hardware device, such as GPIO.</span><li>
     <li><span style="font-size:0.5em" >&bull; &nbsp;&nbsp; Update post-memory policy configuration by using PCD.</span><li>
  </ul> 
 <li><span style="font-size:0.65em" >2.&nbsp;&nbsp; Add board policy update code in <font face="Consolas">@size[.8em](SiliconPolicyUpdatePostMemory &lpar;&rpar;)</font> ,
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font face="Consolas">@size[.7em](BoardPkg/PeiSiliconPolicyUpdateLib /PeiBoardXxxInitLib.c.)</font></span> </li>
  <ul style="list-style-type:none; line-height:0.5;">
     <li><span style="font-size:0.5em" >&bull; &nbsp;&nbsp; The PCD updated in <font face="Consolas">@size[.9em](BoardInitBeforeSiliconInit &lpar;&rpar;)</font> might be used here.</span><li>
  </ul> 
 <li><span style="font-size:0.65em" >3.&nbsp;&nbsp;  Add board initialization DXE code in <font face="Consolas">@size[.7em](BoardInitAfterPciEnumeration &lpar;&rpar;)</font>,
 <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font face="Consolas">@size[.8em](BoardInitReadyToBoot&lpar;&rpar;,   BoardInitEndOfFirmware &lpar;&rpar;)</font> . </span> </li>
   <ul style="list-style-type:none; line-height:0.5;">
     <li><span style="font-size:0.5em" >– Note: The functions may be empty if no updating is required.</span> </li>
   </ul>
 <li><span style="font-size:0.65em" >4.&nbsp;&nbsp;  Ensure all PCDs in the configuration section (DSC files) are correct for your 
  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;board. -  Set <font face="Consolas">@size[.8em](gMinPlatformPkgTokenSpaceGuid.PcdBootStage = 3)</font></span> </li>
 <li><span style="font-size:0.65em" >5.&nbsp;&nbsp;  Ensure all required binaries in the flash file (FDF files) are correct for your 
  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;board.</span> </li>
 <li><span style="font-size:0.65em" >6.&nbsp;&nbsp;  Boot, collect debug log, and verify the test point results are correct.</span> </li>
</ul>

<p style="line-height:70%" align="left" ><span style="font-size:0.45em; ">
<a href="https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/5_stage_3_boot_to_uefi_shell/59_test_point_results.html">EDK II Open Platform Spec Test points Stage 3</a>
</span></p>

@snapend


Note:

Steps to enable a board for Stage III
Add board post-memory initialization code in BoardInitBeforeSiliconInit () and
BoardInitAfterSiliconInit () ,
BoardPkg/BoardInitLib/PeiBoardXxxInitPostMemoryLib.c.
i. Initialize board-specific hardware device, such as GPIO.
ii. Update post-memory policy configuration by using PCD.
2. Add board policy update code in SiliconPolicyUpdatePostMemory () ,
BoardPkg/PeiSiliconPolicyUpdateLib /PeiBoardXxxInitLib.c.
i. The PCD updated in BoardInitBeforeSiliconInit () might be used here.
3. Add board initialization DXE code in BoardInitAfterPciEnumeration () ,
BoardInitReadyToBoot () , BoardInitEndOfFirmware () .
i. NOTE: The functions may be empty if nothing needs to be updated.
4. Ensure all PCDs in the configuration section (DSC files) are correct for your board.
i. Set gMinPlatformPkgTokenSpaceGuid.PcdBootStage = 2
5. Ensure all required binaries in the flash file (FDF files) are correct for your board.
6. Boot, collect debug log, and verify the test point results defined in section 5.9 of the EDK II Open platform spec are
correct.
 

EDK II Open platform spec Test points Stage 3: 
https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/5_stage_3_boot_to_uefi_shell/59_test_point_results.html


---?image=assets/images/slides/Slide_TableDHote.JPG
@title[Staged Approach by Features Section 04 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Staged Approach by Features</b>)</span><br><span style="font-size:0.75em;" >- Platform Firmware Boot Stage PCD</span></p>


@snap[north-west span-50 ]
<br>
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 1&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Enable Debug &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 2&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Memory Initialization)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 3&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot to UEFI Shell only &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Stage 4&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Boot ot OS)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 5&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS w/ Security enabled&nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 6&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Advanced Feature Selection)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 7&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Performance Opetimizations &nbsp;)</span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south-east span-45 ]
<p style="line-height:50%" align="left" ><span style="font-size:0.6em;" >
PCD Is tested within .FDF to see which modules to include 
</span></p>
@snapend



@snap[south-east span-13 ]
<p style="line-height:20%" align="left" ><span style="font-size:02.1em;" >
4
<br><br>
</span></p>
<br><br>
@snapend

Note:
table d’hôte  
Image source: http://3.bp.blogspot.com/-nCzQh7Xu3_I/Uzk1a4DRk-I/AAAAAAAABCY/lQvT1cbn8Ug/s1600/5892-Caucasian-Man-Sitting-At-A-Table-And-Reading-A-Menu-At-A-Restaurant-Clipart-Illustration.jpg



Depending on the stage # provides some idea regarding what components are needed for a BIOS solution. It can be 3M full featured BIOS, or only 256K if just the basic boot is required, in some cases. 

This work can be done by defining some default configuration in PlatformConfig.dsc. 
For example, PcdBootStage|4 can be used to configure a BIOS to support a boot to OS (with ACPI/SMM), or PcdBootStage|3 to configure a BIOS to boot to shell only (without ACPI/SMM) 

- Stage I - Minimal Debug
  - Serial Port, Port 80, External debuggers Optional: Software debugger
- Stage II  - Memory Functional
  - Basic hardware initialization including main memory
- Stage III - Boot to UEFI Shell
   - Generic DXE driver execution
- Stage IV - Boot to OS
  - Boot a general purpose operating system with the minimally required feature set. Publish a minimal set of ACPI tables.- Stage V -Security Enabled
  - UEFI Secure Boot, TCG trusted boot, DMA protection, etc.
- Stage VI - Advanced Feature Selection
  - Firmware update, power management, networking support, manageability, testability, reliability, availability, serviceability, non-essential provisioning and resiliency mechanisms
- Stage VII – Tuning
   - Size and performance optimizations



---?image=assets/images/slides/Slide77.JPG
@title[Boot Flow – Stage 4]
<p align="right"><span class="gold" >@size[1.1em](<b>Boot Flow – Stage 4</b>)</span><span style="font-size:0.75em;" ></span></p>


Note:

The objective of Stage IV is to enable a minimal boot path that successfully boots a
commercial operating system such as Linux or Windows, with UEFI interfaces exposed to
the OS implemented in compliance with the UEFI specification. The minimal boot path only
involves functionality necessary to load the OS to a state where a user may begin
performing more complex interactions. This involves successfully reaching an environment
that allows the user to launch applications. 


The stage does not include support for all
applications that, for example, may require certain CPU or GPU features enabled. Nor does
it require any further support, including but not limited to device and system power
management, full hardware performance support enabled, system reset support, etc.
Any additional functionality is classified as an advanced feature. Those features are
collectively enabled in Stage VI.






---?image=assets/images/slides/Slide78.JPG
@title[High Level Control Flow – Stage 4]
<p align="right"><span class="gold" >@size[1.1em](<b>High Level Control Flow – Stage 4</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-east span-57 ]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.85em; "><br>
Major Execution Activities
</span></p>

<ul style="list-style-type:disc; line-height:0.7;">
  <li><span style="font-size:0.65em" > Minimum ACPI Table Initialization </span> </li>
  <li><span style="font-size:0.65em" > Additional input, output, and storage support based on platform and operating system requirements</span> </li>
  <li><span style="font-size:0.65em" > SMM </span> </li>
  <li><span style="font-size:0.65em" > Perform ACPI enable/disable</span> </li>
  <li><span style="font-size:0.65em" > Kernel debug support</span> </li>
  <li><span style="font-size:0.65em" > UEFI variable support</span> </li>
</ul>
@snapend

Note:


Stage IV introduces additional functionality to meet the minimal requirements for a UEFIcompliant
operating system. Much of the support required will be performed during the DXE
phase interleaving Stage IV control flows with pre-existing control flows from Stage III. A
minimum set of ACPI tables, namely RSDT, FACP, FACS, FADT, MADT, HPET and DSDT,
need to be initialized and published. If there are alternative and/or additional operating
system expectations such as full DeviceTree support, that should be enabled to allow the
operating system to be loaded.


It is recommended that only the mandatory boot option devices are connected in BDS to
minimize complexity and boot time in the minimal execution path to the operating system. In
the flow diagram below, the left half is identical to the functionality enabled by Stage III prior
to entering the BDS phase. It is expected that the Stage III components are reused to
complete Stage IV tasks.


The green blocks on slide Control Flow are reuse of the existing blocks from Stage III




---
@title[Stage 4 Firmware Volumes]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 4 Firmware Volumes</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Name&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Content</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > FvOsBoot&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > Continued DXE/BDS Services&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > FvLateSilicon&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > ACPI and SMM silicon support&nbsp;</span></p></td>
	</tr>
</table>
<br>
<ul style="list-style-type:none; line-height:0.7;">
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp; Finalize silicon initialization</span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp; Add basic operating system required interfaces</span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp; Add support for minimal featured operating system boot. </span> </li>
</ul>

@snapend




Note:

Stage IV finalizes silicon initialization, adds basic operating system required interfaces, and
supports minimally featured operating system boot. The new components are support in a
dedicated firmware volume.



---
@title[Stage 4 Firmware Volumes Contents]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 4 FVs Contents</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>

<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>FV&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Components</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Purpose</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > FvOsBoot&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" > FvLateSilicon.fv&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="70%"><p style="line-height:022%"><span style="font-size:0.45em" > Additional silicon initialization support that is performed late in boot&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; " > List of ACPI modules&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="70%"><p style="line-height:022%"><span style="font-size:0.45em" > ACPI Table, Platform & Board DXE &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; " >List of SMM modules &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="70%"><p style="line-height:022%"><span style="font-size:0.45em" > SmmIpl, SMM Core,SMM CPU etc, (DXE) &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:21%"><span style="font-size:0.4em; " > List Storage media modules&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="70%"><p style="line-height:.02%"><span style="font-size:0.45em" > Sata, USB, . . . , (DXE)&nbsp;</span></p></td>
	</tr>
</table>	
@snapend

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Mapped according to .FDF file layout<br><br>&nbsp;</span></p>)
@snapend


Note:

1.  Late silicon - Additional silicon initialization support that is performed late in the boot
2. ACPI Modules - Acpi Table, platform & Board Dxe 
3. SMM Modules - SmmIpl, SMM Core,SMM CPU etc, DXE 
4. Storage Media - Sata, USB, Bus etc, DXE

https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/6_stage_4_boot_to_os/62_firmware_volumes.html#62-firmware-volumes

for a list of more Modules in the FV for stage 


---
@title[Stage 4 Platform Libraries - PEI]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 4 Platform Architecture Libraries</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.75em;">
Stage 4 Modules - @size[.8em](List of UEFI and DXE Components: <a href="https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/content/appendix_a_full_maps/a1_firmware_volume_layout.html">EDK II Open Platform Spec.</a>)
<br>
<br>
<br>
Stage 4 Platform Architecture Libraries
</span></p>


<table id="recTable-1">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Item</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:30%"><span style="font-size:0.5em" ><b>API Definition</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:30%"><span style="font-size:0.5em" ><b>Producing Pkg</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.5em" ><b>Description</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  BoardAcpiLib</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  MinPlatformPkg</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  BoardPkg</span></p></td>
		<td bgcolor="#121212" height=".02%" width="50%"><p style="line-height:01%"><span style="font-size:0.4em" >   Services for ACPI table creation and SMM enable/dis</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  BoardInitLib</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  MinPlatformPkg</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.4em; font-family:Consolas;" >  BoardPkg</span></p></td>
		<td bgcolor="#121212" height=".02%" width="50%"><p style="line-height:21%"><span style="font-size:0.4em" >Board specific initialization hook at DXE phase for BoardNotificationInit   </span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south span-95 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:70%"><span style="font-size:0.8em">Board porting requires creation of libraries produced <br>by the <font face="Consolas">@size[.85em](BoardPkg)</font> <br>&nbsp;</span></p>)
@snapend


Note:

To find the Libraries for the Platform specific code
1 Search the Work space .DSC files for the string of the library
2 Open the .DSC files associated with the platform
3 Determine which Library is used and that should have the build path in the workspace.

Board porting will require creation of libraries identified as produced by the BoardPkg.


Depending on the board, there may be existing libraries that are sufficient for a board, so it is
important to assess the utility of existing library instances when developing board support.



---
@title[Tips for Board Specific ACPI  ]
<p align="right"><span class="gold" >@size[1.1em](<b> Tips for Board Specific ACPI </b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-east span-70 ]
<br>
<br>
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b>&nbsp;</b><br><br>&nbsp;</span></p>)
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b>&nbsp;</b><br><br>&nbsp;</span></p>)
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b>&nbsp;</b><br><br>&nbsp;</span></p>)
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b>&nbsp;</b><br><br>&nbsp;</span></p>)
@snapend


@snap[north-west span-31 ]
<br>
<br>
@box[bg-royal text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><b>Board Library</b><br><br>&nbsp;</span></p>)
@box[bg-royal text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b> NVS Space</b><br><br>&nbsp;</span></p>)
@box[bg-royal text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b> Special Features</b><br><br>&nbsp;</span></p>)
@box[bg-royal text-white rounded my-box-pad2  ](<p style="line-height:80%"><span style="font-size:0.9em;" ><b> ASL & C In<br> Same  Dir </b><br>&nbsp;</span></p>)
@snapend



@snap[north-east span-68 ]
<br>
<br>
@css[text-white fragment](<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >&bull; Use board specific library for ACPI global NVS area<br>&nbsp;&nbsp; assignments instead defining in ASL Code<br><br></span></p>)
@css[text-white fragment](<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >&bull; Do Not define huge amount of board specific<br>&nbsp;&nbsp; configuration in the global NVS area<br><br><br></span></p>)
@css[text-white fragment](<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >&bull; Board specific devices or advanced features<br>&nbsp;&nbsp;  should be moved to the board specific directory<br><br></span></p>)
@css[text-white fragment](<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >&bull; Use the same directory for the <font face="Consolas">@size[.7em](GlobalNvs.asl)</font><br>&nbsp;&nbsp; and <font face="Consolas">@size[.7em](GobalNvsAreaDef.h)</font>  files<br><br><br></span></p>)
@snapend


Note:

It is not recommended define BoardId in ACPI global NVS and use the board ID check in the ASL code. Use a board specific library instead

Do Not define huge amount of board specific configuration in the global NVS area because a generic platform should not have the board specific knowledge 

If this Global NVS is for a board specific device, it should be moved to the board specific directory. A board should define a board specific NVS, or just use a simple Name object under this device node. 

If this Global NVS is for a board advanced feature, it should be moved to the feature directory. This fetaure driver should define a feature specific NVS, or just use a simple Name object for the feature. 


The Global NVS ASL definition (such as https://github.com/tianocore/edk2-platforms/blob/devel-MinPlatform/Platform/Intel/KabylakeOpenBoardPkg/Include/Acpi/GlobalNvs.asl) and C-language definition (such as https://github.com/tianocore/edk2-platforms/blob/devel-MinPlatform/Platform/Intel/KabylakeOpenBoardPkg/Include/Acpi/GlobalNvsAreaDef.h) should be put to same directory. As such people can compare them to know the mapping between C-language definition and ASL definition. A better is to use a tool to create one from the other to avoid mismatch issue. 




---?image=assets/images/slides/Slide37.JPG
@title[Example: Board Specific ACPI ]
<p align="right"><span class="gold" >@size[1.1em](<b>Example: Board Specific ACPI </b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[south-west span-100 ]
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
<br>
@snapend

@snap[north-east span-95 ]
<p style="line-height:70%" align="left" ><span style="font-size:0.7em" ><br><br>
&bull; &nbsp;&nbsp;Tip: Board specific device selection - define a board-neutral name<br>
&bull; &nbsp;&nbsp;Data structure is board neutral <font face="Consolas">@size[.8em](@color[yellow]( .../Include/Acpi/GlobalNvsAreaDef.h ))</font><br>
&bull; &nbsp;&nbsp;File:&nbsp; <font face="Consolas">@size[.75em](@color[yellow](KabylakeOpenBoardPkg/KabylakeRvp3/Library/BoardAcpiLib/))<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; @size[.75em](@color[yellow](DxeKabylakeRvp3AcpiTableLib.c))</font>
</span></p>

@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<br>
<br>
<p style="line-height:35%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br><br>
VOID<br>
@color[yellow](KabylakeRvp3UpdateGlobalNvs) (<br>
VOID<br>
)<br>
&lbrace; // <font face="Arial">@color[#A8ff60](Update global NVS area for ASL and SMM init code to use)</font> <br>&nbsp;&nbsp;
mGlobalNvsArea.Area = (VOID *)(UINTN)PcdGet64 (PcdAcpiGnvsAddress);<br>&nbsp;&nbsp;
mGlobalNvsArea.Area-&gt;PowerState = 1;<br>&nbsp;&nbsp;
mGlobalNvsArea.Area-&gt;NativePCIESupport = PcdGet8 (PcdPciExpNative);<br>&nbsp;&nbsp;
mGlobalNvsArea.Area-&gt;ApicEnable = GLOBAL_NVS_DEVICE_ENABLE;<br>&nbsp;&nbsp;
mGlobalNvsArea.Area-&gt;LowPowerS0Idle = PcdGet8 (PcdLowPowerS0Idle);<br>&nbsp;&nbsp;
mGlobalNvsArea.Area-&gt;Ps2MouseEnable = FALSE;<br>&nbsp;&nbsp;
mGlobalNvsArea.Area-&gt;Ps2KbMsEnable = PcdGet8 (PcdPs2KbMsEnable);<br>
&rbrace;
</span></p>
@snapend



@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Tip: use board specific library for ACPI NVS Area<br><br>&nbsp;</span></p>)
@snapend


Note:

It is not recommended define BoardId in ACPI global NVS and use the board ID check in the ASL code.

BKM is to define a board-neutral name for the branch condition  
If this device is a silicon device and it might be enabled/disabled by policy, BKM recommended is using the this mechanism. 

Protocol from 
KabylakeOpenBoardPkg/Include/Protocol/GlobalNvsArea.h

Data structure typedef:
KabylakeOpenBoardPkg/Include/Acpi/GlobalNvsAreaDef.h


The other way to resolve above issue is to move the board specific ACPI Secondary System Description Table (SSDT) to the board specific directory and let it be installed by a board specific ACPI driver. The basic platform ACPI driver should only handle generic ACPI tables, like FADT, MCFG, HPET, MCFG, and etc. 

This means the .asi  has to determine specifics
A better way is to keep those board specific SSDT in board directly using a board specific library as the example of this slide


---?image=assets/images/slides/Slide37.JPG
@title[Required Function Interfaces DXE]
<p align="right"><span class="gold" >@size[1.1em](<b>Required Function Interfaces DXE</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-52 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-47 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
MinPlatformPkg/ <br>&nbsp;&nbsp;
 PlatformInit/  <br>&nbsp;&nbsp;&nbsp;&nbsp;
  Library/  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      MultiBoardInitSupportLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         DxeMultiBoardInitSupportLib.c<br>&nbsp;&nbsp;&nbsp;&nbsp;
  PlatformInitDxe/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    PlatformInitDxe.c <br>&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;
       @color[yellow](BoardNotificationInitEntryPoint&lpar;&rpar;)
</span></p>
@snapend

@snap[north-east span-44 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.65em; font-family:Consolas;"><br><br>
@color[yellow](BoardInitLib) <br>
 <br>
</span></p>
<br><br>

<p style="line-height:70%" align="left" ><span style="font-size:0.75em" >
Board specific initialization hook at DXE phase.<br><br>
Notify:<br>
<font face="Consolas">@size[.8em](@color[yellow](OnPciEnumerationComplete ))</font><br>
<font face="Consolas">@size[.8em](@color[yellow](SmmReadyToLockRegistration))</font>
</span></p>

@snapend

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Registers two callbacks to call FSP notifies<br><br>&nbsp;</span></p>)
@snapend


Note:

This routine registers two callbacks to call fsp's notifies


---?image=assets/images/slides/Slide37.JPG
@title[Required SMM Function Interfaces DXE]
<p align="right"><span class="gold" >@size[1.1em](<b>Required SMM Function Interfaces DXE</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-52 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-47 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
KabylakeOpenBoardPkg/ <br>&nbsp;&nbsp;
 KabylakeRvp3/  <br>&nbsp;&nbsp;&nbsp;&nbsp;
  Library/  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      BoardAcpiLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[yellow](SmmBoardAcpiEnableLib.c)<br><br>&nbsp;&nbsp;&nbsp;&nbsp;
		 or<br><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[yellow](SmmMultiBoardAcpiSupportLib.c)<br><br>&nbsp;&nbsp;&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-44 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.65em; font-family:Consolas;"><br><br>
@color[yellow](BoardAcpiEnableLib) <br>
 <br>
</span></p>
<br><br>

<p style="line-height:70%" align="left" ><span style="font-size:0.75em" >
Board specific initialization hook at DXE phase.<br><br>
<br>
<font face="Consolas">@size[.8em](@color[yellow](SiliconEnableAcpi &lpar;&rpar; ))</font><br>
<font face="Consolas">@size[.8em](@color[yellow](SiliconDisableAcpi &lpar;&rpar;))</font>
</span></p>

@snapend


Note:

This routine registers two callbacks to call fsp's notifies


---?image=assets/images/slides/Slide37.JPG
@title[Required SMM Function Interfaces DXE]
<p align="right"><span class="gold" >@size[1.1em](<b>Required SMM Function Interfaces DXE</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-52 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-47 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br>&nbsp;</span></p>)
@snapend


@snap[north-east span-98 ]
<br>
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
Platform/Intel/<br>
KabylakeOpenBoardPkg/ <br>&nbsp;&nbsp;
 KabylakeRvp3/  <br>&nbsp;&nbsp;&nbsp;&nbsp;
  Library/  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      BoardAcpiLib/<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[yellow](DxeBoardAcpiTableLib.c)<br><br>&nbsp;&nbsp;&nbsp;&nbsp;
		 or<br><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         @color[yellow](DxeMultiBoardAcpiSupportLib.c)<br><br>&nbsp;&nbsp;&nbsp;&nbsp;
</span></p>
@snapend

@snap[north-east span-44 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.65em; font-family:Consolas;"><br><br>
@color[yellow](BoardAcpiTableLib) <br>
 <br>
</span></p>
<br><br>

<p style="line-height:70%" align="left" ><span style="font-size:0.75em" >
Board specific initialization hook at DXE phase.<br><br>
<br>
<font face="Consolas">@size[.8em](@color[yellow](BoardUpdateAcpiTable&lpar;&rpar; ))</font><br>
</span></p>

@snapend


Note:

This routine registers two callbacks to call fsp's notifies



---
@title[Stage 4 Checklist  ]
<p align="center"><span class="gold" >@size[1.1em](<b>Stage 4 Checklist</b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; "><br>
Steps to enable a board for Stage 4.
</span></p>

@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

@snap[north-west span-100 ]
<br>
<br>
<br>
<br>
<ul style="list-style-type:None; line-height:0.75;">
 <li><span style="font-size:0.78em" >1.&nbsp;&nbsp; Install the minimal DSDT <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp; In rare cases: Install board-specific SSDT </span></li>
 <li><span style="font-size:0.78em" >2.&nbsp;&nbsp; Ensure all PCDs in the configuration section (DSC files) are<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  correct for your board. <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp; Set <font face="Consolas">@size[.8em](gMinPlatformPkgTokenSpaceGuid.PcdBootStage = 4)</font></span></li>
 <li><span style="font-size:0.78em" >3.&nbsp;&nbsp; Ensure all required binaries in the flash file (FDF files) are<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; correct for your board.</span></li>
 <li><span style="font-size:0.78em" >4.&nbsp;&nbsp; Boot, collect log, verify test point results defined are correct</span></li>
</ul>
<br>
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.45em; ">
<a href="https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/6_stage_4_boot_to_os/69_test_point_results.html">EDK II Open Platform Spec Test points Stage 4</a>
</span></p>

@snapend


Note:


Steps to enable a board for Stage IV
1. Install the minimal DSDT - In rare cases: Install board-specific SSDT
2. Ensure all PCDs in the configuration section (DSC files) are correct for your board. - Set gMinPlatformPkgTokenSpaceGuid.PcdBootStage = 4
3. Ensure all required binaries in the flash file (FDF files) are correct for your board.
4. Boot, collect log, verify test point results defined in section 6.9 Test Point Results are
correct



EDK II Open Platform Spec Test points Stage 4:

https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/6_stage_4_boot_to_os/69_test_point_results.html




---?image=assets/images/slides/Slide_TableDHote.JPG
@title[Staged Approach by Features Section 05 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Staged Approach by Features</b>)</span><br><span style="font-size:0.75em;" >- Platform Firmware Boot Stage PCD</span></p>


@snap[north-west span-50 ]
<br>
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 1&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Enable Debug &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 2&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Memory Initialization)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 3&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot to UEFI Shell only &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 4&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Stage 5&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Boot ot OS w/ Security enabled&nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 6&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Advanced Feature Selection)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 7&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Performance Opetimizations &nbsp;)</span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south-east span-45 ]
<p style="line-height:50%" align="left" ><span style="font-size:0.6em;" >
PCD Is tested within .FDF to see which modules to include 
</span></p>
@snapend



@snap[south-east span-13 ]
<p style="line-height:20%" align="left" ><span style="font-size:02.1em;" >
5
<br><br>
</span></p>
<br><br>
@snapend

Note:
table d’hôte  
Image source: http://3.bp.blogspot.com/-nCzQh7Xu3_I/Uzk1a4DRk-I/AAAAAAAABCY/lQvT1cbn8Ug/s1600/5892-Caucasian-Man-Sitting-At-A-Table-And-Reading-A-Menu-At-A-Restaurant-Clipart-Illustration.jpg



Depending on the stage # provides some idea regarding what components are needed for a BIOS solution. It can be 3M full featured BIOS, or only 256K if just the basic boot is required, in some cases. 

This work can be done by defining some default configuration in PlatformConfig.dsc. 
For example, PcdBootStage|4 can be used to configure a BIOS to support a boot to OS (with ACPI/SMM), or PcdBootStage|3 to configure a BIOS to boot to shell only (without ACPI/SMM) 

- Stage I - Minimal Debug
  - Serial Port, Port 80, External debuggers Optional: Software debugger
- Stage II  - Memory Functional
  - Basic hardware initialization including main memory
- Stage III - Boot to UEFI Shell
   - Generic DXE driver execution
- Stage IV - Boot to OS
  - Boot a general purpose operating system with the minimally required feature set. Publish a minimal set of ACPI tables.- Stage V -Security Enabled
  - UEFI Secure Boot, TCG trusted boot, DMA protection, etc.
- Stage VI - Advanced Feature Selection
  - Firmware update, power management, networking support, manageability, testability, reliability, availability, serviceability, non-essential provisioning and resiliency mechanisms
- Stage VII – Tuning
   - Size and performance optimizations



---?image=assets/images/slides/Slide89.JPG
@title[Boot Flow – Stage 5]
<p align="right"><span class="gold" >@size[1.1em](<b>Boot Flow – Stage 5</b>)</span><span style="font-size:0.75em;" ></span></p>


Note:

The objective of Stage V is to establish the basic system security foundation for a production
environment. Given the importance of security for all connected systems, the platform
architecture considers the following basic security features as minimum requirements for any
product and thus an important part of the effort to produce a minimal platform. This stage is
concerned with enabling security technologies described in industry specifications. Lowerlevel
chipset-specific security technologies such as register locks may exist and those
should be enabled during standard silicon initialization flows in earlier stages.



---?image=assets/images/slides/Slide90.JPG
@title[Stage 5 is Focused on Security ]
<p align="right"><span class="gold" >@size[1.1em](<b>Stage 5 is Focused on Security </b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100]
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em;" >
List of Documents on Security with EDK II -     <a href="https://github.com/tianocore/tianocore.github.io/wiki/EDK-II-Security-White-Papers">EDK II tianocore Wiki </a><br><br>
Minimal security checks should be done
</span></p>
@snapend

@snap[north-west span-70]
<br>
<br>
<p style="line-height:40%" align="left" ><span style="font-size:0.75em;" ><br><br><br><br>
</span></p>

<ul style="list-style-type:disc; line-height:0.7;">
  <li><span style="font-size:0.65em" ><a href="https://github.com/chipsec/chipsec">Chipsec</a> </span> </li>
  <li><span style="font-size:0.65em" > Microsoft Hardware Security Test Interface (HSTI)</span> </li>
  <li><span style="font-size:0.65em" > Windows Security Mitigations Table (WSMT). </span> </li>
  <li><span style="font-size:0.65em" > Memory Attribute Table </span> </li>
  <li><span style="font-size:0.65em" > SMM Memory Attribute Table </span> </li>
  <li><span style="font-size:0.65em" > 3rd party option ROM </span> </li>
  <li><span style="font-size:0.65em" > Trusted Console - Trusted Storage </span> </li>
  <li><span style="font-size:0.65em" > DMA protection for Intel® VT-d/IOMM</span> </li>
  <li><span style="font-size:0.65em" > SMI Handler</span> </li>
  <li><span style="font-size:0.65em" > TPM</span> </li>
  <li><span style="font-size:0.65em" > Firmware Update</span> </li>
</ul>
<br>
<br>
@snapend


Note:


Once the board porting work is finished, some minimal security checks should be done to make sure there is not security hole



---
@title[Stage 5 Porting - Goals]
<p align="right"><span class="gold" >@size[1.1em](<b>Stage 5 Porting - Goals</b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em;" >
Satisfy industry standard security specifications 
</span></p>

@snap[north-west span-85 ]
<br>
<br>
<br>
<br>
@box[bg-royal text-white rounded my-box-pad2 fragment ](<p style="line-height:60%" ><span style="font-size:0.75em;" >&nbsp;&nbsp;Establish a Static Root of Trust for Verification (S-RTV)  <br>&nbsp;</span></p>)
@box[bg-royal text-white rounded my-box-pad2 fragment ](<p style="line-height:60%" ><span style="font-size:0.75em;" >&nbsp;&nbsp;Static Root of Trust for Measurement (S-RTM) <br>&nbsp;</span></p>)
@box[bg-royal text-white rounded my-box-pad2 fragment ](<p style="line-height:60%" ><span style="font-size:0.75em;" >&nbsp;&nbsp;Direct Memory Access (DMA) Protection  <br>&nbsp;</span></p>)
@snapend


Note:

Stage V introduces new modules and requirements to the boot incrementally over Stage IV.

The key requirement is to satisfy industry standard security specifications applicable to the
platform. The security technologies enabled in this stage are not strictly bound to the
definition in this specification and may consist of a subset or superset of the content
described in this section. However, the only case in which a modern production system
should not implement a form of any of these technologies is if the necessary hardware is not
available. In all other cases, the system must at least implement a form of the following

Goals -
-  Hardware rooted authenticated boot that can establish a Static Root of Trust for Verification (S-RTV) and continue an authenticated chain of verification throughout the boot process.
-  System measurement capability that allows the firmware to serve as a Static Root of Trust for Measurement (S-RTM).
-  Protection from Direct Memory Access (DMA) attacks.



---
@title[Stage 5 – Security- Features ]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 5 – Security- Features </b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-east span-70  ]
<br>
<br>
<br>
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b>&nbsp;</b><br><br><br>&nbsp;</span></p>)
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b>&nbsp;</b><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-west span-31 fragment ]
<br>
<br>
<br>
@box[bg-green-pp text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><b><br>TCG trusted boot</b><br><br>&nbsp;</span></p>)
@snapend



@snap[north-east span-68 fragment]
<br>
<br>
<br>
@css[text-white ](<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >TCG measured boot chain of trust should be enabled in this stage.<br><br><br></span></p>)
@snapend


@snap[north-west span-31 fragment]
<br>
<br>
<br>
@box[bg-green-pp text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><b><br>TCG trusted boot</b><br><br>&nbsp;</span></p>)
@box[bg-green-pp text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b><br> UEFI Secure Boot</b><br><br>&nbsp;</span></p>)
@snapend



@snap[north-east span-68 fragment]
<br>
<br>
<br>
@css[text-white ](<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >TCG measured boot chain of trust should be enabled in this stage.<br><br><br></span></p>)
@css[text-white ](<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >Authenticated UEFI Variable support must be completely functional. This is a basic requirement for secure authentication and UEFI Secure Boot key management<br><br><br></span></p>)
@snapend


Note:

The TCG measured boot chain of trust should be enabled in this stage. 


At this point,
Authenticated UEFI Variable support must be completely functional. This is a basic
requirement for secure authentication and management of the UEFI Secure Boot keys.



---
@title[Stage 5 Firmware Volumes]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 5 Firmware Volumes</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Name&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Content</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >  FvSecurity&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > Security related modules&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;&nbsp;  FvSecurityPreMemory&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;&nbsp;  FvSecurityPostMemory&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;&nbsp;  FvSecurityLate&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >  NvStorage&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > Real NV storage on flash&nbsp;</span></p></td>
	</tr>
</table>
<br>

<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >
Supports key security features
</span></p>


@snapend




Note:

Stage V supports key secutiy features.



---
@title[Stage 5 Firmware Volumes Contents]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 5 FVs Contents</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>

<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:.10%"><span style="font-size:0.65em" ><b>FV&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:.10%"><span style="font-size:0.65em" ><b>Components</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:.10%"><span style="font-size:0.65em" ><b>Purpose</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > FvSecurity&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="35%"><p style="line-height:01%"><span style="font-size:0.4em;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:022%"><span style="font-size:0.45em" >  &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="35%"><p style="line-height:01%"><span style="font-size:0.4em;" > List of TCG modules&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:022%"><span style="font-size:0.45em" >  TPM Services, Config, Platform, etc&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="35%"><p style="line-height:01%"><span style="font-size:0.4em;" > List of Intel&reg; VT-d modules&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:022%"><span style="font-size:0.45em" > IOMMU PEI & DXE Services &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="35%"><p style="line-height:01%"><span style="font-size:0.4em;" > List Security modules&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:022%"><span style="font-size:0.45em" > Provide security architecture protocol Secure boot UI config. . . &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" > &nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="35%"><p style="line-height:01%"><span style="font-size:0.4em;" > List of variable SMM modules&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%" width="40%"><p style="line-height:022%"><span style="font-size:0.45em" >  Fault-tolerant, Variable,  SMM Services&nbsp;</span></p></td>
	</tr>
</table>	
@snapend

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Mapped according to .FDF file layout<br><br>&nbsp;</span></p>)
@snapend


Note:

see :
https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/7_stage_5_security_enable/72_firmware_volumes.html 

for a list of more Modules in the FV for stage 

---
@title[Modules – Stage 5 ]
<p align="right"><span class="gold" >@size[1.1em](<b> Modules – Stage 5 </b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-east span-70 ]
<br>
<br>
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b>&nbsp;</b><br><br><br>&nbsp;</span></p>)
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b>&nbsp;</b><br><br><br><br>&nbsp;</span></p>)
@box[bg-grey-15 text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b>&nbsp;</b><br><br><br>&nbsp;</span></p>)
@snapend


@snap[north-west span-33 ]
<br>
<br>
@box[bg-navy text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b> PEI Components </b><br><br>&nbsp;</span></p>)
<br>
@box[bg-navy text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b> DXE Components </b><br><br>&nbsp;</span></p>)
<br>
@box[bg-navy text-white rounded my-box-pad2  ](<p style="line-height:60%"><span style="font-size:0.9em;" ><b> SMM Components </b><br><br>&nbsp;</span></p>)
@snapend



@snap[north-east span-65 ]
<br>
<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" ><br>
&bull; &nbsp;&nbsp; Tcg2 Pei – SecurityPkg<br>
&bull; &nbsp;&nbsp; Tcg2 platform Pei – PlatformPkg<br>
&bull; &nbsp;&nbsp; Intel Vt-d PMR - SiliconPkg
<br><br><br>
</span></p>
<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >
&bull; &nbsp;&nbsp; Tcg2 DXE  – SecurityPkg<br>
&bull; &nbsp;&nbsp; Tcg2 platform Dxe – PlatformPkg<br>
&bull; &nbsp;&nbsp; SecureBootConfigDxe -SecurityPkg<br>
&bull; &nbsp;&nbsp; Intel Vt-d Dxe- SiliconPkg<br>
<br>
</span></p>
<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >
&bull; &nbsp;&nbsp; Tcg2 SMM  – SecurityPkg<br>
&bull; &nbsp;&nbsp; FaultTolerantWriteSMM<br>
&bull; &nbsp;&nbsp; VariableSMM<br>
<br><br>
</span></p>

@snapend


Note:

Only modules in the board package should be modified in the process of board porting. The
minimum platform package and other common package contents must not be directly
modified. The board package and silicon package modules may have multiple instances to
support different boards and different silicon. These components are required. They enable
orderly board porting and add the support for extensibility in later stages. The libraries
consumed are the subset of libraries required by this specification. Some libraries are
defined in this specification, some are defined in EDK II documentation.




---
@title[Stage 5 Required Functions]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 5 Required Functions</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<p style="line-height:20%" align="left" ><span style="font-size:0.2em;" >&nbsp;
</span></P>
<table id="recTable-1">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:.010%"><span style="font-size:0.5em" ><b>Phase</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:.010%"><span style="font-size:0.5em" ><b>Name</b> &nbsp;</span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:.010%"><span style="font-size:0.5em" ><b>Purpose</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" > PEI </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" >  PeimEntryMA ()</span></p></td>
		<td bgcolor="#121212" height=".02%" width="60%"><p style="line-height:01%"><span style="font-size:0.4em" >   Entry point for the TPM2 PEIM</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" >  &nbsp; </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" >  IntelVTdPmrInitialize ()&nbsp; </span></p></td>
		<td bgcolor="#121212" height=".02%" width="60%"><p style="line-height:01%"><span style="font-size:0.4em" >   Entry point for the VT-d PEIM&nbsp; </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" >  DXE&nbsp; </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" >  DriverEntry ()&nbsp; </span></p></td>
		<td bgcolor="#121212" height=".02%" width="60%"><p style="line-height:01%"><span style="font-size:0.4em" >  Entry point for the TPM2 DXE module&nbsp;  </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" >  &nbsp; </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" >  IntelVTdInitialize()&nbsp; </span></p></td>
		<td bgcolor="#121212" height=".02%" width="60%"><p style="line-height:01%"><span style="font-size:0.4em" >  Entry point for the VT-d DXE module &nbsp; </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" > &nbsp;  </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" > UserPhysicalPresent()&nbsp;  </span></p></td>
		<td bgcolor="#121212" height=".02%" width="60%"><p style="line-height:01%"><span style="font-size:0.4em" >  Indicates whether a physical user is present for UEFI secure boot &nbsp; </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" > &nbsp;  </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:22%"><span style="font-size:0.4em; font-family:Consolas;" > ProcessTcgPp & ProcessTcgMor&nbsp;  </span></p></td>
		<td bgcolor="#121212" height=".02%" width="60%"><p style="line-height:22%"><span style="font-size:0.4em" >   ProcessTcgPp Process the TPM physical presence (PP) request & memory overwrite request (MOR)&nbsp; </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" > SMM&nbsp;  </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" > InitializeTcgSmm ()&nbsp;  </span></p></td>
		<td bgcolor="#121212" height=".02%" width="60%"><p style="line-height:01%"><span style="font-size:0.4em" >   Entry point for the TPM2 SMM module&nbsp; </span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" > &nbsp;  </span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:.01%"><span style="font-size:0.4em; font-family:Consolas;" > MemoryClearCallback ()&nbsp;  </span></p></td>
		<td bgcolor="#121212" height=".02%" width="60%"><p style="line-height:01%"><span style="font-size:0.4em" >   Callback function for setting the MOR variable &nbsp; </span></p></td>
	</tr>
</table>
<br>
@snapend



Note:
The following functions are required to exist and to execute in the given order. The
component that provides the function is not specified because it is not required by the
architecture.

All except ProcessTcgPp & ProcessTcgMor are in the EDK II Common open source code 




Depending on the board, there may be existing libraries that are sufficient for a board, so it is
important to assess the utility of existing library instances when developing board support.

---
@title[Security Related PCDs and Variables ]
<p align="right"><span class="gold" >@size[1.1em](<b>Security Related PCDs and Variables</b>)</span><span style="font-size:0.75em;" ></span></p>
<ul style="list-style-type:disc; line-height:0.8;">
  <li><span style="font-size:0.75em" > Authenticated Variables – UEFI Secure Boot </span> </li>
  <ul style="list-style-type:none; line-height:0.6;">
    <li><span style="font-size:0.55em; font-family:Consolas;" >&bull;&nbsp;&nbsp; PK, KEK, db and dbx </span> </li>
  </ul>

  <li><span style="font-size:0.75em" > TPM - Policy: TCG trusted boot </span> </li>
  <ul style="list-style-type:none; line-height:0.6;">
    <li><span style="font-size:0.55em; font-family:Consolas;" >&bull;&nbsp;&nbsp; PcdTpmInstanceGuid, PcdTpm2InitializationPolicy, PcdTpm2SelfTestPolicy</span> </li>
  </ul>

  <li><span style="font-size:0.75em" > Memory Only Reset (MOR)- Policy: TCG MOR</span> </li>
  <ul style="list-style-type:none; line-height:0.6;">
    <li><span style="font-size:0.55em; font-family:Consolas;" >&bull;&nbsp;&nbsp; PRE_MEM_SILICON_POLICY, L"MemoryOverwriteRequestControl"</span> </li>
  </ul>

  <li><span style="font-size:0.75em" > Intel® VT-d – DMA protection </span> </li>
  <ul style="list-style-type:none; line-height:0.6;">
    <li><span style="font-size:0.55em; font-family:Consolas;" >&bull;&nbsp;&nbsp; PcdVTdPolicyPropertyMask</span> </li>
  </ul>

</ul>

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Definitions may be both source and binary <br><br>&nbsp;</span></p>)
<br>
@snapend

Note:

These definitions may be both source and binary in nature.

https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/7_stage_5_security_enable/75_configuration.html#75-configuration

- Authenticated Variables – UEFI Secure Boot
  - PK, 
  - KEK, 
  - db and dbx
- TPM - Policy: TCG trusted boot
  - PcdTpmInstanceGuid, 
  - PcdTpm2InitializationPolicy, 
  - PcdTpm2SelfTestPolicy
- Memory Only Reset (MOR ) - Policy: TCG MOR
  - PRE_MEM_SILICON_POLICY, L“MemoryOverwriteRequestControl”
- Intel® VT-d – DMA protection 
   - PcdVTdPolicyPropertyMask


---
@title[Security Feature Related PCDs ]
<p align="right"><span class="gold" >@size[1.1em](<b>Security Feature Related PCDs</b>)</span><span style="font-size:0.75em;" ></span></p>
<br>
<ul style="list-style-type:disc; line-height:0.8;">
  <li><span style="font-size:0.75em" > Enable SMI handler profile </span> </li>
  <ul style="list-style-type:none; line-height:0.6;">
    <li><span style="font-size:0.55em; font-family:Consolas;" >&bull;&nbsp;&nbsp; gMinPlatformModuleTokenSpaceGuid.PcdSmiHandlerProfileEnable </span> </li>
  </ul>
  <li><span style="font-size:0.75em" >Enable TPM   </span> </li>
  <ul style="list-style-type:none; line-height:0.6;">
    <li><span style="font-size:0.55em; font-family:Consolas;" >&bull;&nbsp;&nbsp;  gMinPlatformModuleTokenSpaceGuid.PcdTpm2Enable</span> </li>
  </ul>

  <li><span style="font-size:0.75em" > Enable UEFI Secure boot </span> </li>
  <ul style="list-style-type:none; line-height:0.6;">
    <li><span style="font-size:0.55em; font-family:Consolas;" >&bull;&nbsp;&nbsp;  gMinPlatformModuleTokenSpaceGuid.PcdUefiSecureBootEnable</span> </li>
  </ul>

</ul>

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Enable/Disable in <font face="Consolas">@size[.8em](OpenBoardPkgConfig.dsc)</font <br><br>&nbsp;</span></p>)
<br>
@snapend

Note:

https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/7_stage_5_security_enable/75_configuration.html#75-configuration





---
@title[Stage 5 Checklist  ]
<p align="center"><span class="gold" >@size[1.1em](<b>Stage 5 Checklist</b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; ">Steps to enable a board for Stage 5:</span></p>

@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

@snap[north-west span-100 ]
<br>
<br>
<br>
<ul style="list-style-type:None; line-height:0.65;">
 <li><span style="font-size:0.7em" >1.&nbsp;&nbsp; Update <font face="Consolas">@size[.8em](@color[yellow](BoardPkg/Board))</font>. </span></li>
 <ul style="list-style-type:none; line-height:0.56;">
    <li><span style="font-size:0.55em; " >&bull;&nbsp;&nbsp; Deploy the UEFI secure boot variables (PK/KEK/db/dbx)</span> </li>
    <li><span style="font-size:0.55em; " >&bull;&nbsp;&nbsp; Configure <font face="Consolas">@size[.8em](@color[yellow](PcdTpmInstanceGuid))</font> to select TPM hardware. 
	     Default value of <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font face="Consolas">@size[.8em](@color[yellow](gEfiTpmDeviceInstanceTpm20DtpmGuid))</font> is usually correct.</span> </li>
 </ul>
 <li><span style="font-size:0.7em" >2.&nbsp;&nbsp; UEFI secure boot:</span></li>
 <ul style="list-style-type:none; line-height:0.56;">
      <li><span style="font-size:0.55em; " >&bull;&nbsp;&nbsp;Update <font face="Consolas">@size[.8em](PlatformSecureLib : @color[yellow](UserPhysicalPresent&lpar;&rpar;))</font> to check if a user is 
      physically present <br>&nbsp;&nbsp;&nbsp;&nbsp;to authorize change of authenticated variables.</span></li>
 </ul>
 <li><span style="font-size:0.7em" >3.&nbsp;&nbsp; For TCG Trusted Boot:</span></li>
 <ul style="list-style-type:none; line-height:0.56;">
    <li><span style="font-size:0.55em; " >&bull;&nbsp;&nbsp; May select TPM2 instance <font face="Consolas">@size[.8em](@color[yellow](PcdTpmInstanceGuid))</font>.</span> </li>
    <li><span style="font-size:0.55em; " >&bull;&nbsp;&nbsp; May set <font face="Consolas">@size[.8em](@color[yellow](PcdFirmwareDebuggerInitialized))</font> 
	based on whether or not a Firmware Debugger is <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;attached to platform</span> </li>
 </ul>
 <li><span style="font-size:0.7em" >4.&nbsp;&nbsp; For DMA Protection: include IOMMU driver for DMA protection, if silicon <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;supports IOMM</span></li>
 <li><span style="font-size:0.7em" >5.&nbsp;&nbsp; Ensure all PCDs in configuration section (DSC files) are correct for <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;your board. Set <font face="Consolas">@size[.8em](@color[yellow](MinPlatformPkgTokenSpaceGuid.PcdBootStage = 5))</font></span></li>
 <li><span style="font-size:0.7em" >6.&nbsp;&nbsp; Ensure all required binaries in the flash file (FDF files) are correct for <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;your board.</span></li>
 <li><span style="font-size:0.7em" >7.&nbsp;&nbsp; Boot, collect log, verify test point results are correct.</span></li>
</ul>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.45em; ">
<a href="https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/7_stage_5_security_enable/79_test_point_results.html">EDK II Open Platform Spec Test points Stage 5</a>
</span></p>

@snapend


Note:
Steps to enable a board for Stage V
1. Update BoardPkg/Board. 
  - Deploy the UEFI secure boot variables (PK/KEK/db/dbx)
  - Configure PcdTpmInstanceGuid to select TPM hardware. Default of gEfiTpmDeviceInstanceTpm20DtpmGuid value is usually correct.
2. UEFI secure boot -  Update PlatformSecureLib : UserPhysicalPresent () , to check if a user is physically present to authorize change of authenticated variables
3. For TCG trusted boot
  - May select TPM2 instance PcdTpmInstanceGuid .
  - May set PcdFirmwareDebuggerInitialized based on whether or not a Firmware Debugger is attached to the platform
4. For DMA Protection -  May include IOMMU driver to do DMA protection, if the silicon supports IOMMU.
5. Ensure all PCDs in the configuration section (DSC files) are correct for your board. - Set MinPlatformPkgTokenSpaceGuid.PcdBootStage = 5
6. Ensure all required binaries in the flash file (FDF files) are correct for your board.
7. Boot, collect log, verify test point results are Correct





---?image=assets/images/slides/Slide_TableDHote.JPG
@title[Staged Approach by Features Section 06 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Staged Approach by Features</b>)</span><br><span style="font-size:0.75em;" >- Platform Firmware Boot Stage PCD</span></p>


@snap[north-west span-50 ]
<br>
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 1&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Enable Debug &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 2&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Memory Initialization)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 3&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot to UEFI Shell only &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 4&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 5&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS w/ Security enabled&nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Stage 6&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Advanced Feature Selection)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 7&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Performance Opetimizations &nbsp;)</span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south-east span-45 ]
<p style="line-height:50%" align="left" ><span style="font-size:0.6em;" >
PCD Is tested within .FDF to see which modules to include 
</span></p>
@snapend



@snap[south-east span-13 ]
<p style="line-height:20%" align="left" ><span style="font-size:02.1em;" >
6
<br><br>
</span></p>
<br><br>
@snapend

Note:
table d’hôte  
Image source: http://3.bp.blogspot.com/-nCzQh7Xu3_I/Uzk1a4DRk-I/AAAAAAAABCY/lQvT1cbn8Ug/s1600/5892-Caucasian-Man-Sitting-At-A-Table-And-Reading-A-Menu-At-A-Restaurant-Clipart-Illustration.jpg



Depending on the stage # provides some idea regarding what components are needed for a BIOS solution. It can be 3M full featured BIOS, or only 256K if just the basic boot is required, in some cases. 

This work can be done by defining some default configuration in PlatformConfig.dsc. 
For example, PcdBootStage|4 can be used to configure a BIOS to support a boot to OS (with ACPI/SMM), or PcdBootStage|3 to configure a BIOS to boot to shell only (without ACPI/SMM) 

- Stage I - Minimal Debug
  - Serial Port, Port 80, External debuggers Optional: Software debugger
- Stage II  - Memory Functional
  - Basic hardware initialization including main memory
- Stage III - Boot to UEFI Shell
   - Generic DXE driver execution
- Stage IV - Boot to OS
  - Boot a general purpose operating system with the minimally required feature set. Publish a minimal set of ACPI tables.- Stage V -Security Enabled
  - UEFI Secure Boot, TCG trusted boot, DMA protection, etc.
- Stage VI - Advanced Feature Selection
  - Firmware update, power management, networking support, manageability, testability, reliability, availability, serviceability, non-essential provisioning and resiliency mechanisms
- Stage VII – Tuning
   - Size and performance optimizations



---?image=assets/images/slides/Slide101.JPG
@title[Boot Flow – Stage 6]
<p align="right"><span class="gold" >@size[1.1em](<b>Boot Flow – Stage 6</b>)</span><span style="font-size:0.75em;" ></span></p>


Note:

#### Stage 6 for Advanced Features

Advanced features are non-essential features. Essential features are defined as being
support required to meet earlier stage boot objectives. An advanced feature must be
implemented as highly cohesive and stand-alone software to only support a specific feature.
Modularizing such features, reducing dependencies on other advanced features, and
eliminating dependencies on specific implementations of other advanced features is critical
and results in a variety of benefits:



---
@title[Add Non-essential Features - Stage 6 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Add Non-essential Features - Stage 6</b>)</span><span style="font-size:0.75em;" ></span></p>
@snap[north-west span-49 ]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.8em;" >
<b>Examples: Core Features</b>
</span></p>
<ul style="list-style-type:none; line-height:0.8;">
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;Signed Capsule update</span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;Signed Recovery</span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;Source Debug Enable</span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;NVMe (secondary storage)</span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;eMMC (secondary storage)</span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;S3 resume</span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;Network</span> </li>
</ul>

@snapend


@snap[north-east span-53 ]
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.8em;" >
&nbsp;&nbsp;<b>Platform Features</b>
</span></p>
<ul style="list-style-type:none; line-height:0.8; text-align: left;">
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;SMBIOS </span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;Intel® Active Management &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;@color[black](.)<br>&nbsp;&nbsp;&nbsp;&nbsp;Technology (AMT) </span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;Thunderbolt™ </span> </li>
</ul>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.8em;" >
&nbsp;&nbsp;<b>Board Features</b>
</span></p>
<ul style="list-style-type:none; line-height:0.8; text-align: left;">
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;Embedded Controller&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; @color[black](.)</span> </li>
  <li><span style="font-size:0.75em" >&bull;&nbsp;&nbsp;Setup (policy) </span> </li>
</ul>
@snapend

@snap[south span-85 fragment]
@box[bg-purple-pp text-white rounded my-box-pad2  ](<p style="line-height:40%"><span style="font-size:0.8em">Limit  required features to reduce complexity<br><br>&nbsp;</span></p>)
<br>
@snapend

Note:

high-level examples of advanced features

The number of "advanced features" in a platform should be limited to what is required and reasonable to reduce the
required level of design and validation complexity.


---?image=assets/images/slides/Slide103.JPG
@title[Advanced Feature Requirements]
<p align="right"><span class="gold" >@size[1.1em](<b>Advanced Feature Requirements</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-100 ]
<br>
<br>
<br>
<p style="line-height:60%" align="left"><span style="font-size:0.85em;" >
Each advanced feature:
</span></p>
<ul style="list-style-type:none; line-height:0.85;">
  <li class="fragment"><span style="font-size:0.7em" >&bull;&nbsp;&nbsp; Has low coupled component interactions</span> </li>
  <li class="fragment"><span style="font-size:0.7em" >&bull;&nbsp;&nbsp; Complete, mutually independent and only depend on packages <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; in edk2 repository</span> </li>
  <li class="fragment"><span style="font-size:0.7em" >&bull;&nbsp;&nbsp; Organized as cohesive packages related to the same advanced feature</span> </li>
  <li class="fragment"><span style="font-size:0.7em" >&bull;&nbsp;&nbsp; Support enabling individually as part of porting within stage 6</span> </li>
  <li class="fragment"><span style="font-size:0.7em" >&bull;&nbsp;&nbsp; Possible to distribute independently in binary form –  add/remove PCD <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Switch</span> </li>
  <li class="fragment"><span style="font-size:0.7em" >&bull;&nbsp;&nbsp; Self-documenting – contains a ReadMe.md template</span> </li>
</ul>
@snapend


Note:
https://62e528761d0685343e1c-f3d1b99a743ffa4142d9d7f1978d9686.ssl.cf2.rackcdn.com/files/16476/width668/vx477nkd-1350018704.jpg

- Advanced features must be a complete feature.
  - Fractions of functionality such as libraries that plug into a module defined in another package are not features.
- Advanced features may only depend on packages in edk2.
  - DEC files outside edk2 shall not be referenced in an advanced feature.
- Advanced features shall be organized in cohesive packages related to the feature
domain.
      - Informative examples: DebugFeaturePkg, IoFeaturePkg, PowerManagementFeaturePkg
      - New feature packages must be proposed as an RFC to the community mailing list. The proposal shall include the package name, purpose, maintainers and reviewers, and identify any pre-existing packages that will be moved to the feature. The maintainers of any packages affected by the proposal must be included in the RFC notification list. If the feature proposal is well received, it must be ratified in the TianoCore Design Meeting. If approved, the RFC author should follow through to implement the change.

Advanced features must be mutually independent.

Advanced features must support being enabled on an individual basis when Stage VI is
enabled.

- Advanced features must be distributed in a binary independent manner such that the
feature can be added and removed at the binary level (recommendation is with a single
FeaturePcd).
- Advanced features must be self-documenting. Each feature must include a ReadMe.md
in the root directory that describes the feature using the template described in this
section.
- Advanced features must fail in a graceful and developer friendly manner




---
@title[Advanced Feature Design ]
<p align="right"><span class="gold" >@size[1.1em](<b>Advanced Feature Design</b>)</span><br>
<span style="font-size:0.75em;" >- Feature Template Readme.md </span></p>


@snap[north-west span-30 ]
<br>
<br>
<br>
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Firmware Volumes<br>&nbsp;</span></p>)
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Modules <br>&nbsp;</span></p>)
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Required Functions<br>&nbsp;</span></p>)
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Configuration<br>&nbsp;</span></p>)
@snapend

@snap[north span-30 ]
<br>
<br>
<br>
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Data Flows<br>&nbsp;</span></p>)
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Control Flows<br>&nbsp;</span></p>)
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Build Files<br>&nbsp;</span></p>)
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Test Point Results<br>&nbsp;</span></p>)
@snapend


@snap[north-east span-30 ]
<br>
<br>
<br>
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Functional Exit Criteria<br>&nbsp;</span></p>)
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Feature Enabling Checklist<br>&nbsp;</span></p>)
@box[bg-blue-pp text-white rounded my-box-pad2 ](<p style="line-height:60%" ><span style="font-size:0.7em;" >&nbsp;&nbsp; Common Optimizations<br>&nbsp;</span></p>)
@snapend

Note:

Define an advanced feature using the template as shown on this slide. This template should be included in feature review and placed in the feature root directory as README.md – 
Next slide has details


Advanced features should be designed such that they are easily portable between minimum platform compliant implementations. In consideration of portability, it is recommended to encapsulate each feature within a dedicated package. Such encapsulation enables rapid integration of the feature and a focused area for feature-related changes. For example, feature declarations for build elements such as GUIDs, PCDs, PPIs, and protocols are scoped within the feature package DEC file. Including the feature and consequently the
package imports the feature tokens within the available namespace and changes affecting the feature are localized to the package which in turn exposes the change to all feature consumers.



- Firmware Volumes - The binary containers needed for the feature.
- Modules  - The EDK II component binaries and static libraries required.
- Required Functions - Functions that are useful for understanding, porting, or debugging the feature and how these key functions are integrated into the Stage I-V required functions.
- Configuration - The configurable parameters for a given feature.
- Data Flows - The architecturally defined data structures and flows for a given feature.
- Control Flows - Key control flows for the feature.
- Build Files - The DSC/FDF for integrating the feature.
- Test Point Results - The test that can verify porting is complete for the feature.
- Functional Exit Criteria - The testable functionality for the feature.
- Feature Enabling Checklist - The required activities to achieve desired functionality for the feature.
- Common Optimizations - Common size or performance tuning options for this feature.



The Advanced Feature template should be used to describe relevant configuration for integrating the feature into a minimum platform compliant system. Any board or silicon specific details should be abstracted such that the information is provided to the feature via "feature APIs". Such dependencies are recommended to be exposed via binary interfaces such as PPIs and protocols and can be considered similar in purpose to the architectural PPIs and Protocols defined in the PI specification. Such requirements must be included in
the "Required Functions" section of the advanced feature template. Though not required, to increase portability, advanced features should not depend upon deprecated EDK II packages and attempt to reduce exposure to packages other than MdePkg and UefiCpuPkg. In turn, this decreases risk of depending upon deprecated packages in the future 


+++
@title[Advanced Feature Design 02 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Advanced Feature Design</b>)</span><br>
<span style="font-size:0.75em;" >- Feature Template Readme.md </span></p>
<p style="line-height:60%" align="left"><span style="font-size:0.7em;" >
This template should be included in feature review and placed in the feature root directory as README.md
</span></p>

@snap[north-west span-49 ]
<br><br>
<p style="line-height:50%" align="left"><span style="font-size:0.56em;" ><br><br><br>
@color[yellow](Firmware Volumes) - The binary containers needed for the feature.<br>
@color[yellow](Modules)  - The EDK II component binaries and static libraries required.<br>
@color[yellow](Required Functions) - Functions that are useful for understanding, porting, or debugging the feature and how these key functions are integrated into the Stage I-V required functions.<br>
@color[yellow](Configuration) - The configurable parameters for a given feature.<br>
@color[yellow](Data Flows) - The architecturally defined data structures and flows for a given feature.<br>
@snapend



@snap[north-east span-49 ]
<br><br>
<p style="line-height:50%" align="left"><span style="font-size:0.56em;" ><br><br><br>
@color[yellow](Control Flows) - Key control flows for the feature.<br>
@color[yellow](Build Files) - The DSC/FDF for integrating the feature.<br>
@color[yellow](Test Point Results) - The test that can verify porting is complete for the feature.<br>
@color[yellow](Functional Exit Criteria) - The testable functionality for the feature.<br>
@color[yellow](Feature Enabling Checklist) - The required activities to achieve desired functionality for the feature.<br>
@color[yellow](Common Optimizations) - Common size or performance tuning options for this feature.<br>
@snapend

Note:
Advanced features should be designed such that they are easily portable between minimum platform compliant implementations. In consideration of portability, it is recommended to encapsulate each feature within a dedicated package. Such encapsulation enables rapid integration of the feature and a focused area for feature-related changes. For example, feature declarations for build elements such as GUIDs, PCDs, PPIs, and protocols are scoped within the feature package DEC file. Including the feature and consequently the
package imports the feature tokens within the available namespace and changes affecting the feature are localized to the package which in turn exposes the change to all feature consumers.


The Advanced Feature template should be used to describe relevant configuration for integrating the feature into a minimum platform compliant system. Any board or silicon specific details should be abstracted such that the information is provided to the feature via "feature APIs". Such dependencies are recommended to be exposed via binary interfaces such as PPIs and protocols and can be considered similar in purpose to the architectural PPIs and Protocols defined in the PI specification. Such requirements must be included in
the "Required Functions" section of the advanced feature template. Though not required, to increase portability, advanced features should not depend upon deprecated EDK II packages and attempt to reduce exposure to packages other than MdePkg and UefiCpuPkg. In turn, this decreases risk of depending upon deprecated packages in the future 


+++
@title[Advanced Feature Design 02 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Advanced Feature Design</b>)</span><br>
<span style="font-size:0.75em;" >- Feature Template Readme.md </span></p>
<p style="line-height:60%" align="left"><span style="font-size:0.7em;" >
This template should be included in feature review and placed in the feature root directory as README.md - <i>@size[.7em](&nbsp;copy and paste below)</i>
</span></p>

```
### Firmware Volumes 
- The binary containers needed for the feature.
### Modules  
- The EDK II component binaries and static libraries required.
### Required Functions 
- Functions that are useful for understanding, porting, or debugging the feature and how these key functions are integrated into the Stage I-V required functions.
### Configuration 
- The configurable parameters for a given feature.
### Data Flows 
- The architecturally defined data structures and flows for a given feature.
### Control Flows 
- Key control flows for the feature.
### Build Files 
- The DSC/FDF for integrating the feature.
### Test Point Results 
- The test that can verify porting is complete for the feature.
### Functional Exit Criteria 
- The testable functionality for the feature.
### Feature Enabling Checklist 
- The required activities to achieve desired functionality for the feature.
### Common Optimizations 
- Common size or performance tuning options for this feature.

```

Note:

copy and past to readme.md


---
@title[Stage 6 Firmware Volumes]
<p align="right"><span class="gold" >@size[1.1em](<b> Stage 6 Firmware Volumes</b>)</span><span style="font-size:0.75em;" ></span></p>


@snap[north-west span-100 ]
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Name&nbsp;</b></span></p></td>
		<td bgcolor="#0070C0" ><p style="line-height:10%"><span style="font-size:0.65em" ><b>Content</b> &nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >  FvAdvanced&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > Advanced feature softwarae stacks&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;&nbsp;  FvAdvancedPreMemory&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > Stage 1 SEC PEI&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;&nbsp;  FvAdvancedPostMemory&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > Stage 2 PEI  DXE&nbsp;</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em; font-family:Consolas;" >&nbsp;&nbsp;&nbsp;  FvAdvancedLate&nbsp;</span></p></td>
		<td bgcolor="#121212" height=".02%"><p style="line-height:01%"><span style="font-size:0.5em" > Stage 3-4 DXE UEFI / OS&nbsp;</span></p></td>
	</tr>
</table>
<br>

<p style="line-height:60%" align="left" ><span style="font-size:0.7em;" >
Advanced Features should be modular to these stages of the boot flow
</span></p>

@snapend




Note:
The PEI core will create a FV HOB for each child firmware volume such that each DXE
firmware volume is exposed to the DXE dispatcher


---
@title[Example – Adding Network]
<p align="right"><span class="gold" >@size[1.1em](<b> Example – Adding Network</b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:65%" align="left"><span style="font-size:0.7em;" >
@size[1.1em](The Network stack modules are board and silicon independent thus no porting is necessary.  Feature is capable with Stage 3-4.)<br><br>
 1. &nbsp;&nbsp;Set PCDs: <br>
  <font face="Consolas">&nbsp;&nbsp;&nbsp;
  @size[.78em](gAdvancedFeaturePkgTokenSpaceGuid.PcdNetworkEnable|TRUE)<br>&nbsp;&nbsp;&nbsp;
  @size[.78em](gEfiMdeModulePkgTokenSpaceGuid.PcdEfiNetworkSupport|TRUE)<br>
  </font>
 2. &nbsp;&nbsp;Add the network modules to the board <font face="Consolas">.dsc and .fdf</font> within the<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Stage 6 FV <br>
 3. &nbsp;&nbsp;Common <font face="Consolas">.dsc and .fdf</font> include files found in <font face="Consolas">edk2/NetworkPkg</font><br>
 <font face="Consolas">&nbsp;&nbsp;&nbsp;
  @size[.8em](&bull;&nbsp;&nbsp;NetworkDefines.dsc.inc)<br>&nbsp;&nbsp;&nbsp;
  @size[.8em](&bull;&nbsp;&nbsp;NetworkPcds.dsc.inc)<br>&nbsp;&nbsp;&nbsp;
  @size[.8em](&bull;&nbsp;&nbsp;NetworkPkg/NetworkLibs.dsc.inc)<br>&nbsp;&nbsp;&nbsp;
  @size[.8em](&bull;&nbsp;&nbsp;NetworkPkg/NetworkComponents.dsc.inc)<br>&nbsp;&nbsp;&nbsp;
  @size[.8em](&bull;&nbsp;&nbsp;Network.fdf.inc)<br>
 </font>
 4. &nbsp;&nbsp;Add appropriate "<font face="Consolas">@size[.8em](!include)</font>" statements to <font face="Consolas">@size[.8em](OpenBoardPkg.dsc & .fdf)</font>
<br>
</span></p>


Note:

gEfiMdeModulePkgTokenSpaceGuid.PcdEfiNetworkSupport|TRUE
        This Causes PciBus driver to skip loading network option ROM if set FALSE.



---
@title[Example Include Network in Board .DSC]
<p align="right"><span class="gold" >@size[1.1em](<b>Example Include Network in Board .DSC</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-95 ]
<br>
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend



@snap[north-east span-98 ]
<br>
<br>
<p style="line-height:45%" align="left" ><span style="font-size:0.45em; font-family:Consolas;">
@size[1.4em](OpenBoardPkg.dsc)<br><br>
 . . .<br>
[Defines]<br>
@color[cyan](!include NetworkPkg/NetworkDefines.dsc.inc)<br>
. . .<br>
<br>
[LibraryClasses.common]<br>
@color[cyan](!include NetworkPkg/NetworkLibs.dsc.inc)<br>
<br>
. . .<br>
<br>
[Components.X64]<br>
@color[cyan](!include NetworkPkg/NetworkComponents.dsc.inc)<br>
</span></p>
<br>

<p style="line-height:65%" align="left"><span style="font-size:0.7em;" >
Add the NetworkPkg "<font face="Consolas">!include</font>" file statements in the sections shown 
</span></p>

@snapend


Note:

Add the NetworkPkg !include statements in the sections shown of the OpenBoardPkg.dsc file

---
@title[Example Include Network in Board .FDF]
<p align="right"><span class="gold" >@size[1.1em](<b>Example Include Network in Board .FDF</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-95 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend



@snap[north-east span-98 ]
<br>
<p style="line-height:40%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
@size[1.4em](OpenBoardPkg.fdf)<br>
 . . .<br>
[FV.@color[yellow](FvAdvancedLate)]<br>
. . .<br>
FvNameGuid         = 05411CAD-6C35-4675-B6CA-8748032144B4<br>
@color[cyan](!include NetworkPkg/Network.fdf.inc)<br>
. . .<br>
[FV.FvAdvanced]<br>
. . .<br>
FvNameGuid         = B23E7388-9953-45C7-9201-0473DDE5487A<br>
. . .<br>
FILE FV_IMAGE = 07FC4960-5322-4DDC-A6A4-A17DE492DFE3 &lbrace;<br> &nbsp;&nbsp;&nbsp;&nbsp;
       SECTION GUIDED EE4E5898-3914-4259-9D6E-DC7BD79403CF <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
           PROCESSING_REQUIRED = TRUE &lbrace;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
         SECTION FV_IMAGE = @color[yellow](FvAdvancedLate)<br>&nbsp;&nbsp;&nbsp;&nbsp;
       &rbrace;<br>&nbsp;&nbsp;
     &rbrace;<br>



</span></p>
<br>

<p style="line-height:65%" align="left"><span style="font-size:0.7em;" >
Add the NetworkPkg "<font face="Consolas">!include</font>" file statements in the section shown 
</span></p>

@snapend


Note:



Add the NetworkPkg !include statements in the FV section,FvAdvancedLate, as  shown of the OpenBoardPkg.fdf file

FvAdvancedLate for the Stage 3-4 (DXE)


---
@title[Example – Disable Some Network Features]
<p align="right"><span class="gold" >@size[1.1em](<b>Example – Disable Some Network Features</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-95 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br>&nbsp;</span></p>)
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br>&nbsp;</span></p>)

@snapend



@snap[north-east span-98 ]
<br>
<p style="line-height:40%" align="left" ><span style="font-size:0.45em; font-family:Consolas;"><br>
<font face="Arial">@size[1.3em](Remove IPv4 in )</font> @size[1.2em](OpenBoardPkg.dsc)<br><br>
 . . .<br>
[Defines]<br>&nbsp;&nbsp;
!include NetworkPkg/NetworkDefines.dsc.inc<br>&nbsp;&nbsp;&nbsp;&nbsp;
  @color[cyan](DEFINE NETWORK_IP4_ENABLE = FALSE)<br><br>
<br>
<font face="Arial">@size[1.3em](Remove ISCSI in )</font>@size[1.2em](OpenBoardPkg.dsc)<br><br>
 . . .<br>
[Defines]<br>&nbsp;&nbsp;
!include NetworkPkg/NetworkDefines.dsc.inc<br>&nbsp;&nbsp;&nbsp;&nbsp;
  @color[cyan](DEFINE NETWORK_ISCSI_ENABLE = FALSE)
<br><br> 
</span></p>
<br>
<p style="line-height:65%" align="left"><span style="font-size:0.7em;" >
The NetworkPkg/NetworkDefines.dsc.inc will set these defines to TRUE
</span></p>

@snapend


Note:

The NetworkPkg/NetworkDefines.dsc.inc will set these defines to TRUE when they are included in the various sections of the OpenBoardPkg.dsc as on the previous slide

---
@title[Example – Adding Thunderbolt™]
<p align="right"><span class="gold" >@size[1.1em](<b>Example – Adding Thunderbolt™</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-100 ]
<br>
<br>
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-98 ]
<br>
<p style="line-height:65%" align="left"><span style="font-size:0.67em;" >
Thunderbolt is a specific feature for the Kabylake
</span></p>
<p style="line-height:30%" align="left" ><span style="font-size:0.4em; font-family:Consolas;">
<font face="Arial">@size[1.3em](Set )</font> @size[1.2em](@color[yellow](gBoardModuleTokenSpaceGuid.PcdTbtEnable|TRUE) in OpenBoardPkgConfig.dsc)<br><br>
@size[1.4em](OpenBoardPkg.dsc)<br><br><br>
@color[yellow](!if gBoardModuleTokenSpaceGuid.PcdTbtEnable == TRUE)<br>
&num; Enable For Thunderbolt(TM) <br>
[LibraryClasses.common]<br>&nbsp;&nbsp;
  TbtCommonLib|KabylakeOpenBoardPkg/Features/Tbt/Library/PeiDxeSmmTbtCommonLib/TbtCommonLib.inf<br>&nbsp;&nbsp;
  DxeTbtPolicyLib|KabylakeOpenBoardPkg/Features/Tbt/Library/DxeTbtPolicyLib/DxeTbtPolicyLib.inf<br>
<br>
[LibraryClasses.IA32]<br>&nbsp;&nbsp;
  PeiTbtPolicyLib|KabylakeOpenBoardPkg/Features/Tbt/Library/PeiTbtPolicyLib/PeiTbtPolicyLib.inf<br>&nbsp;&nbsp;
  PeiDTbtInitLib|KabylakeOpenBoardPkg/Features/Tbt/Library/Private/PeiDTbtInitLib/PeiDTbtInitLib.inf<br>
<br>
[Components.IA32]<br>&nbsp;&nbsp;
  KabylakeOpenBoardPkg/Features/Tbt/TbtInit/Pei/PeiTbtInit.inf<br>
<br>
[Components.X64]<br>&nbsp;&nbsp;
  KabylakeOpenBoardPkg/Features/Tbt/TbtInit/Smm/TbtSmm.inf<br>&nbsp;&nbsp;
  KabylakeOpenBoardPkg/Features/Tbt/TbtInit/Dxe/TbtDxe.inf<br>&nbsp;&nbsp;
  KabylakeOpenBoardPkg/Features/PciHotPlug/PciHotPlug.inf<br>
@color[yellow](!endif)
</span></p>
@snapend


Note:
Add the Tbt libraries and modules within the “if” as shown.
This could be done at the end of the .dsc file 

---
@title[Example – Adding Thunderbolt™]
<p align="right"><span class="gold" >@size[1.1em](<b>Example – Adding Thunderbolt™</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north-west span-52 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)

@snapend

@snap[north-east span-47 ]
<br>
<br>
<br>
@box[bg-black text-white rounded my-box-pad2  ](<p style="line-height:60% "><span style="font-size:0.9em;" ><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;</span></p>)

@snapend


@snap[north-east span-98 ]
<br>
<p style="line-height:30%" align="left" ><span style="font-size:0.4em; font-family:Consolas;"><br>
@size[1.4em](OpenBoardPkg.fdf)<br><br>
. . .<br>
[FV.@color[yellow](FvAdvancedPreMem)]<br>
. . .<br>
FvNameGuid = 6053D78A-457E-4490-A237-31D0FBE2F305<br>
<br>
!if gBoardModuleTokenSpaceGuid.PcdTbtEnable == TRUE<br>
@color[cyan](INF. . ./Features/Tbt/TbtInit/Pei/PeiTbtInit.inf)<br>
!endif<br>
<br>
. . .<br>
<br>
[FV.@color[yellow](FvAdvancedLate)]<br>
. . .<br>
FvNameGuid = 6053D78A-457E-4490-A237-31D0FBE2F305<br>
<br>
!if gBoardModuleTokenSpaceGuid.PcdTbtEnable == TRUE<br>
@color[cyan](INF. . ./Features/Tbt/TbtInit/Dxe/TbtDxeinf)<br>
@color[cyan](INF. . ./Features/PciHotPlug/PciHotPlug.inf)<br>
@color[cyan](INF. . ./Features/Tbt/TbtInit/Smm/TbtSmm.inf)<br>
!endif
</span></p>
@snapend


@snap[north-east span-44 ]
<br>
<p style="line-height:30%" align="left" ><span style="font-size:0.4em; font-family:Consolas;"><br><br><br><br>
[FV.FvAdvanced]<br>
. . .<br>
FvNameGuid         = B23E7388-9953-45C7- . . .<br>
FILE FV_IMAGE = 35E7406A-5842-4F2B . . . &lbrace;<br>&nbsp;&nbsp;
       SECTION FV_IMAGE = @color[yellow](FvAdvancedPreMem)<br>&nbsp;
     &rbrace;<br>
<br>
FILE FV_IMAGE = F5DCB34F-27EA-48AC . . . &lbrace;<br>&nbsp;&nbsp;
       SECTION FV_IMAGE = FvAdvancedPostMem<br>&nbsp;
     &rbrace;<br>
<br>
FILE FV_IMAGE = 07FC4960-5322-4DDC- . . . &lbrace;<br>&nbsp;&nbsp;
       SECTION GUIDED EE4E5898-3914-425 . . .<br>&nbsp;&nbsp;&nbsp;&nbsp;
           PROCESSING_REQUIRED = TRUE &lbrace;<br>&nbsp;&nbsp;&nbsp;
         SECTION FV_IMAGE = @color[yellow](FvAdvancedLate)<br>&nbsp;&nbsp;
       &rbrace;<br>&nbsp;
     &rbrace;
</span></p>
@snapend



Note:


Add the Tbt modules within the “if” as shown within the sections of the FV 



---
@title[Stage 6 Checklist  ]
<p align="center"><span class="gold" >@size[1.1em](<b>Stage 6 Checklist</b>)</span><span style="font-size:0.75em;" ></span></p>
<p style="line-height:70%" align="left" ><span style="font-size:0.75em; ">Steps to enable a board for Stage 6: </span></p>

@snap[north-east span-13]
![Porting_task_list.gif](/assets/images/tenor.gif)
@snapend

@snap[north-west span-100 ]
<br>
<br>
<br>
<br>
<ul style="list-style-type:None; line-height:0.7;">
 <li><span style="font-size:0.7em" >1.&nbsp;&nbsp; Set <font face="Consolas">@color[yellow](gMinPlatformPkgTokenSpaceGuid.PcdBootStage = 6)</font></span></li>
 <li><span style="font-size:0.7em" >2.&nbsp;&nbsp; If required, create board specific library class instance for feature.</span></li>
 <li><span style="font-size:0.7em" >3.&nbsp;&nbsp; Add appropriate updates to PCDs and library class implementations  to<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font face="Consolas">BoardXxx .dsc</font> files</span></li>
 <li><span style="font-size:0.7em" >4.&nbsp;&nbsp; Add required modules to appropriate FV sections in <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font face="Consolas">OpenBoardPkg.fdf</font></span></li>
 <li><span style="font-size:0.7em" >5.&nbsp;&nbsp; Verify Feature enabled is added to build (check Build Directory)</span></li>
 <li><span style="font-size:0.7em" >6.&nbsp;&nbsp; Verify the feature added functionally works.  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This may require several tests depending on the added feature.</span></li>
</ul>
<br>
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.65em; "><i>Updates depend on the features being added</i> </span></p>

@snapend


Note:
Steps to enable a board for Stage VI
1. Depends on the features being added.
2. Basically make sure it builds then check if the added feature functionally works.




---?image=assets/images/slides/Slide_TableDHote.JPG
@title[Staged Approach by Features Section 07 ]
<p align="right"><span class="gold" >@size[1.1em](<b>Staged Approach by Features</b>)</span><br><span style="font-size:0.75em;" >- Platform Firmware Boot Stage PCD</span></p>


@snap[north-west span-50 ]
<br>
<br>
<br>
<br>
<table id="recTable">
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 1&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Enable Debug &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 2&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Memory Initialization)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 3&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot to UEFI Shell only &nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 4&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 5&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Boot ot OS w/ Security enabled&nbsp;)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Stage 6&nbsp;)</span></p></td>
		<td bgcolor="#323232"><p style="line-height:10%"><span style="font-size:0.56em" >@color[#808080](Advanced Feature Selection)</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Stage 7&nbsp;)</span></p></td>
		<td bgcolor="#121212"><p style="line-height:10%"><span style="font-size:0.56em" >@color[yellow](Performance Opetimizations &nbsp;)</span></p></td>
	</tr>
</table>
<br>
@snapend


@snap[south-east span-45 ]
<p style="line-height:50%" align="left" ><span style="font-size:0.6em;" >
PCD Is tested within .FDF to see which modules to include 
</span></p>
@snapend


@snap[south-east span-13 ]
<p style="line-height:20%" align="left" ><span style="font-size:02.1em;" >
7
<br><br>
</span></p>
<br><br>
@snapend

Note:
table d’hôte  
Image source: http://3.bp.blogspot.com/-nCzQh7Xu3_I/Uzk1a4DRk-I/AAAAAAAABCY/lQvT1cbn8Ug/s1600/5892-Caucasian-Man-Sitting-At-A-Table-And-Reading-A-Menu-At-A-Restaurant-Clipart-Illustration.jpg



Depending on the stage # provides some idea regarding what components are needed for a BIOS solution. It can be 3M full featured BIOS, or only 256K if just the basic boot is required, in some cases. 

This work can be done by defining some default configuration in PlatformConfig.dsc. 
For example, PcdBootStage|4 can be used to configure a BIOS to support a boot to OS (with ACPI/SMM), or PcdBootStage|3 to configure a BIOS to boot to shell only (without ACPI/SMM) 

- Stage I - Minimal Debug
  - Serial Port, Port 80, External debuggers Optional: Software debugger
- Stage II  - Memory Functional
  - Basic hardware initialization including main memory
- Stage III - Boot to UEFI Shell
   - Generic DXE driver execution
- Stage IV - Boot to OS
  - Boot a general purpose operating system with the minimally required feature set. Publish a minimal set of ACPI tables.- Stage V -Security Enabled
  - UEFI Secure Boot, TCG trusted boot, DMA protection, etc.
- Stage VI - Advanced Feature Selection
  - Firmware update, power management, networking support, manageability, testability, reliability, availability, serviceability, non-essential provisioning and resiliency mechanisms
- Stage VII – Tuning
   - Size and performance optimizations



---
@title[Stage 7 - Tuning for Performance]
<p align="right"><span class="gold" >@size[1.1em](<b>Stage 7 - Tuning for Performance</b>)</span><span style="font-size:0.75em;" ></span></p>

@snap[north span-80 ]
<br>
<br>
<br>
@box[bg-royal text-white rounded my-box-pad2 fragment ](<p style="line-height:60%" ><span style="font-size:0.75em;" >&nbsp;&nbsp;  Check which features are needed and disable unsupported features<br>&nbsp;</span></p>)
@box[bg-royal text-white rounded my-box-pad2 fragment ](<p style="line-height:60%" ><span style="font-size:0.75em;" >&nbsp;&nbsp;  Removed unused components from the defined Firmware Volumes<br>&nbsp;</span></p>)
@box[bg-royal text-white rounded my-box-pad2 fragment ](<p style="line-height:60%" ><span style="font-size:0.75em;" >&nbsp;&nbsp;  Use available tools to perform detailed analysis of performance and size<br>&nbsp;</span></p>)
<br>
<p style="line-height:70%" align="left" ><span style="font-size:0.5em; ">See EDK II Open Platform Spec <a href="https://edk2-docs.gitbooks.io/edk-ii-minimum-platform-specification/9_stage_7_tuning/">Stage 7: Tuning</a> </span></p>

@snapend


Note:

First, it can be worthwhile to look at the embedded features and performance oriented
options that have been designed into the core or minimum platform. For example, if you do
not support network boot, the PciBus driver provides a PCD to disable dispatching the
network option ROM. By default, network option ROM dispatch is enabled. This is a known
tunable setting.


Second, it can be worthwhile to strip unused components from the defined FV. For simplicity
and consistency of progressing through Stage VI, it is better to use the provided code
consistent with the architecture. Once a stable and fully functional system is completed, it is
intended that platform architecture compatible systems can still remove unneeded
components in order to finely tune the product. The core provides a tool named FMMT that
can be used to process the build output and remove unnecessary components. Alternatively,
a board can copy and modify the provided Build DSC and FDF files in the MinPlatformPkg
and SiliconPkg. The former increases build time. The latter increases integration effort for
new core, MinPlatformPkg, and SiliconPkg releases.



Third, it is often necessary to enable and use tools to perform detailed analysis of
performance and size to identify hotspots that need to be improved.
EDK II Minimum Platform Specification[DRAFT] 9 Stage VII: Tuning
DRAFT


---  
@title[Summary]
<BR>
### <p align="center"<span class="gold"   >Summary </span></p><br>

<!---  Add bullets using https://fontawesome.com/cheatsheet certificate
-->
<ul style="list-style-type:none">
 <li>@fa[certificate gp-bullet-yellow]<span style="font-size:0.9em">&nbsp;&nbsp;Define the porting task list for porting existing <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;open platforms in EDK II</span> </li>
 <li>@fa[certificate gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Determine the necessary porting for each stage <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&amp; boot phase of a new EDK II open platform project </span></li>
</ul>


---?image=assets/images/gitpitch-audience.jpg
@title[Questions]
<br>
![Questions](/assets/images/questions.JPG) 

---
@title[return to main]
<p align="center"><span class="gold"   >@size[1.2em](<b>Return to Main Training Page</b>)</span></p>
<br>
<br>
<br>
<br>
<br>
<p align="center"><span style="font-size:0.9em">Return to Training Table of contents for next presentation <a href="https://github.com/tianocore-training/Tianocore_Training_Contents/wiki#schedule--outline">link</a></span></p>

@snap[north span-30 ]
<br>
<br>
<br>
<a href="https://github.com/tianocore-training/Tianocore_Training_Contents/wiki#schedule--outline">
![trainingLogo](/assets/images/returnTrainingLogo.png)</a>
@snapend


---?image=assets/images/gitpitch-audience.jpg
@title[Logo Slide]
<br><br><br>
![Logo Slide](/assets/images/TianocoreLogo.png =10x)


---
@title[Acknowledgements]
#### <p align="center"><span class="gold"   >Acknowledgements</span></p>

```c++
/**
Redistribution and use in source (original document form) and 'compiled' forms (converted
to PDF, epub, HTML and other formats) with or without modification, are permitted provided
that the following conditions are met:

Redistributions of source code (original document form) must retain the above copyright 
notice, this list of conditions and the following disclaimer as the first lines of this 
file unmodified.

Redistributions in compiled form (transformed to other DTDs, converted to PDF, epub, HTML
and other formats) must reproduce the above copyright notice, this list of conditions and 
the following disclaimer in the documentation and/or other materials provided with the 
distribution.

THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR IMPLIED 
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND 
FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL TIANOCORE PROJECT BE 
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES 
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, 
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, 
WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF ADVISED OF THE POSSIBILITY 
OF SUCH DAMAGE.

Copyright (c) 2019, Intel Corporation. All rights reserved.
**/

```
