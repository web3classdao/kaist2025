# Guide for using HackMD and a markdown file

## English part
HackMD provides an easy interface for writing markdown documents. Even if you don't know the exact markdown syntax, you can easily write documents. However, we recommend that you take this opportunity to familiarize yourself with markdown syntax. The output of many AI services is in markdown format.
- [Markdown Syntax](https://www.markdownguide.org/basic-syntax/)
- [HackMD Tutorial](https://hackmd.io/c/tutorials/%2Fs%2Ftutorials)

HackMD has the ability to collaborate on markdown documents and sync them to Github. For each case study project, I will share two markdown documents, both of which have a report template applied. If it's a Grass project, I'll share the following two files.
- grass.md (English version of the report, by default)
- grass_kr.md (Korean version of the report, optional)

Only the student working on the project will be emailed a link to access the MD file. Clicking the link will open the HackMD editing window, but you won't be able to edit it unless you're signed up for HackMD. Please sign up for HackMD with the email you shared, and you'll have editing permissions and be able to create the document.

The instructor will have read/write access to all documents, so they'll know in real time what you're working on, and he can synchronize with the class website Github to update it when needed. You'll then be able to see the results of your work on the class website.

The samples of the Grass documentation is shaed as a reference for everyone to see. Open the link below to see the markdown document that the Grass report was created from. You will be able to view the editing screen, but cannot edit it. The documents have utilized most of the markdown syntax, so feel free to copy & paste what you need.
- [sample_grass.md](https://hackmd.io/@web3classdao/Skoqa_fHxg/edit)
- [sample_grass_en.md](https://hackmd.io/@web3classdao/BJXg0OfHxl/edit)

There are a few things to keep in mind when writing markdown documents on HackMD. When your document is rendered on the web, a makrdown parser called MkDocs will read your document. So you need to write it in a form that MkDocs can recognize. It is slightly different from the syntax that HackMD understands. Just be careful with the following parts (this is where the HackMD tutorial differs a bit from the one below).
- If you want to add images and resize them, you'll need to use HTML syntax.
    - `<img src="https://hackmd.io/_uploads/S1cF34ZBlg.png" alt="Grass" width="50%">`
    - If you don't need to resize the image, you can follow the [HackMD tutorial](https://hackmd.io/c/tutorials/%2F%40docs%2Finsert-image-in-team-note).
- To create a sublist in Ordered/Unordered Lists, you need to put exactly 4 spaces (or 1 tab).
    - This is so the webpage will represent them correctly.
- In Ordered Lists, the lists should be numbered 1,2,3, etc.

HackMD expires sessions frequently, which is annoying. Whenever it happens, you have to do CAPTCHA. If you feel like HackMD isn't doing well, refresh your browser and do CAPTCHA.

---

## 한국어 파트
HackMD는 markdown 문서를 쉽게 작성할 수 있는 인터페이스를 제공합니다. 당신이 마크다운 문법을 정확히 몰라도 쉽게 문서를 작성할 수 있습니다. 하지만 이번 기회에 마크다운 문법에 익숙해 지는걸 추천합니다. 다양한 AI 서비스의 출력이 마크다운 형식입니다. 
- [Markdown Syntax](https://www.markdownguide.org/basic-syntax/)
- [HackMD Tutorial](https://hackmd.io/c/tutorials/%2Fs%2Ftutorials)

HackMD는 마크다운 문서를 공동작업하고 Github으로 Sync할 수 있는 기능이 있습니다. 각 case study 프로젝트별로 두 개의 마크다운 문서를 공유해 드릴 것입니다. 두 개 모두 보고서 템플릿이 적용되어 있습니다. 만약 Grass 프로젝트라면 아래 두개의 파일이 공유됩니다.
- grass.md (영어 버전의 보고서, 디폴트)
- grass_kr.md (한글 버전의 보고서, 옵션)

프로젝트를 담당하는 학생만 해당 md 파일 접속 링크가 메일로 공유됩니다. 링크를 클릭하면 HackMD 편집창이 열리는데 HackMD에 가입한 상태가 아니면 편집이 안될 것입니다. 공유받은 이메일로 HackMD를 가입해 주세요. 그러면 편집 권한이 생기고 문서를 작성할 수 있습니다.

교수는 모든 문서의 Read/Write 권한이 있기 때문에 문서 작성 현황을 실시간으로 알 수 있습니다. 그리고 필요할 때 수업 웹사이트 Github과 동기화해서 업데이트할 수 있습니다. 그러면 여러분은 수업 웹사이트에서 작업한 결과를 볼 수 있습니다. 

레퍼런스로 작성한 Grass 문서의 샘플을 모두가 볼 수 있게 공유합니다. 아래 링크를 열면 Grass 보고서가 작성된 마크다운 문서를 볼 수 있습니다. 편집화면을 볼 수는 있는만 편집은 안됩니다. 대부분의 마크다운 문법을 활용해 작성했으니 필요한 부분을 복사&붙여넣기 하세요.
- [sample_grass.md](https://hackmd.io/@web3classdao/Skoqa_fHxg/edit)
- [sample_grass_kr.md](https://hackmd.io/@web3classdao/BJXg0OfHxl/edit)

HackMD에서는 마크다운 문서를 작성하실 때 유의할 부분이 있습니다. 최종적으로 웹에서 렌더링할 때는 Github에서 MkDocs라는 마크다운 파서가 문서를 읽기 때문에 MkDocs에서 인식할 수 있는 형태로 작성해야 합니다. 아래 부분 정도를 조심해 주시면 됩니다. (이 부분이 HackMD 튜토리얼과 약간 차이가 나는 부분입니다.)
- 이미지 추가해서 사이즈를 바꾸고 싶으면 HTML 문법을 이용해야 합니다. 
    - `<img src="https://hackmd.io/_uploads/S1cF34ZBlg.png" alt="Grass" width="50%">`
    - 이미지 사이즈 조정이 필요없다면 [HackMD 튜토리얼](https://hackmd.io/c/tutorials/%2F%40docs%2Finsert-image-in-team-note) 대로 하면 됩니다. 
- Ordered/Unordered Lists에서 하위 리스트를 만들려면 4개의 공백(또는 1개의 탭) 을 정확히 넣어야 합니다. 
    - 그래야 웹페이지에서 제대로 표현해 줍니다. 
- Ordered Lists에서 리스트는 1,2,3 등으로 넘버링해줘야 합니다.  

HackMD는 세션 만료가 자주 됩니다. 그때마다 캡차 화면이 뜨는데 귀찮더라도 어쩔 수 없네요. HackMD가 원하는 동작을 하지 않는다고 생각되면 브라우저 Refresh를 해 주세요. 
