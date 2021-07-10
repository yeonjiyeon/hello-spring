<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>스프링 입문 정리</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	text-indent: -1.7em;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC', 'Noto Sans CJK KR'; }

.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Consolas, "Liberation Mono", Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC', 'Noto Sans Mono CJK KR'; }

.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC', 'Noto Sans CJK KR'; }

.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC', 'Noto Sans Mono CJK KR'; }

.highlight-default {
}
.highlight-gray {
	color: rgb(155,154,151);
}
.highlight-brown {
	color: rgb(100,71,58);
}
.highlight-orange {
	color: rgb(217,115,13);
}
.highlight-yellow {
	color: rgb(223,171,1);
}
.highlight-teal {
	color: rgb(15,123,108);
}
.highlight-blue {
	color: rgb(11,110,153);
}
.highlight-purple {
	color: rgb(105,64,165);
}
.highlight-pink {
	color: rgb(173,26,114);
}
.highlight-red {
	color: rgb(224,62,62);
}
.highlight-gray_background {
	background: rgb(235,236,237);
}
.highlight-brown_background {
	background: rgb(233,229,227);
}
.highlight-orange_background {
	background: rgb(250,235,221);
}
.highlight-yellow_background {
	background: rgb(251,243,219);
}
.highlight-teal_background {
	background: rgb(221,237,234);
}
.highlight-blue_background {
	background: rgb(221,235,241);
}
.highlight-purple_background {
	background: rgb(234,228,242);
}
.highlight-pink_background {
	background: rgb(244,223,235);
}
.highlight-red_background {
	background: rgb(251,228,228);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(55, 53, 47, 0.6);
	fill: rgba(55, 53, 47, 0.6);
}
.block-color-brown {
	color: rgb(100,71,58);
	fill: rgb(100,71,58);
}
.block-color-orange {
	color: rgb(217,115,13);
	fill: rgb(217,115,13);
}
.block-color-yellow {
	color: rgb(223,171,1);
	fill: rgb(223,171,1);
}
.block-color-teal {
	color: rgb(15,123,108);
	fill: rgb(15,123,108);
}
.block-color-blue {
	color: rgb(11,110,153);
	fill: rgb(11,110,153);
}
.block-color-purple {
	color: rgb(105,64,165);
	fill: rgb(105,64,165);
}
.block-color-pink {
	color: rgb(173,26,114);
	fill: rgb(173,26,114);
}
.block-color-red {
	color: rgb(224,62,62);
	fill: rgb(224,62,62);
}
.block-color-gray_background {
	background: rgb(235,236,237);
}
.block-color-brown_background {
	background: rgb(233,229,227);
}
.block-color-orange_background {
	background: rgb(250,235,221);
}
.block-color-yellow_background {
	background: rgb(251,243,219);
}
.block-color-teal_background {
	background: rgb(221,237,234);
}
.block-color-blue_background {
	background: rgb(221,235,241);
}
.block-color-purple_background {
	background: rgb(234,228,242);
}
.block-color-pink_background {
	background: rgb(244,223,235);
}
.block-color-red_background {
	background: rgb(251,228,228);
}
.select-value-color-default { background-color: rgba(206,205,202,0.5); }
.select-value-color-gray { background-color: rgba(155,154,151, 0.4); }
.select-value-color-brown { background-color: rgba(140,46,0,0.2); }
.select-value-color-orange { background-color: rgba(245,93,0,0.2); }
.select-value-color-yellow { background-color: rgba(233,168,0,0.2); }
.select-value-color-green { background-color: rgba(0,135,107,0.2); }
.select-value-color-blue { background-color: rgba(0,120,223,0.2); }
.select-value-color-purple { background-color: rgba(103,36,222,0.2); }
.select-value-color-pink { background-color: rgba(221,0,129,0.2); }
.select-value-color-red { background-color: rgba(255,0,26,0.2); }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="2780270f-8073-4170-8c88-9e944bd880d4" class="page sans"><header><h1 class="page-title">스프링 입문 정리</h1></header><div class="page-body"><h3 id="a23e30cf-98a8-47de-9ddb-e9162d92e7c6" class="">1.프로젝트 환경설정</h3><p id="4b92fb1a-81f8-48cf-9624-9fd2f89bfe12" class=""><strong>1-1.프로젝트 환경설정</strong>
<a href="https://start.spring.io/">https://start.spring.io/</a>
스프링관련 프로젝트를 만들어 주는 사이트</p><p id="155f0b58-6406-4d00-a482-2ecb60ceefd5" class="">
</p><p id="f47883c2-244a-4ad4-aecb-90211f22be2a" class="">-maven or gradle
필요한 라이브러리를 땡겨서 오고 빌드하는 라이프사이클까지 관리해주는 툴
버전설정하고 라이브러리를 땡겨오는 것
요즘은 gradle을 더 많이 사용한다</p><p id="4f5f7ec1-3b48-404d-a735-c7297cc9bd05" class="">-Project Metadata
-Group : 그룹에는 보통 기업 도메인명을 적는다</p><p id="c29d146e-4a2f-45bf-bde3-ad0b2c568259" class="">-Dependencies: 어떤 라이브러리를 땡겨서 쓸 것인지 설정</p><p id="0eb6039b-762d-445f-907a-65b703009172" class="">-Thymeleaf: 템플릿 엔진</p><p id="b8767014-0a98-443d-9846-919ee46bb845" class="">-파일구조 : main, test 형식으로 되어있다<div class="indented"><p id="da3e554e-e167-4676-9709-943cd1e462a1" class="">main에 java, resources
java밑에 실제 소스코드들이 있다
resources : 자바파일 외 소스코드들이 들어있다 ex) html
test 코드들과 관련된 소스들이 들어간다, 요즘에는 중요함</p></div></p><p id="e626f63c-a9f6-49a9-8fcd-aa786a5e7df6" class="">&lt;build.gradle&gt;</p><pre id="094ab0e8-3ffc-4259-b718-21cd806e6a20" class="code"><code>
sourceCompatibility = &#x27;11&#x27;  --&gt; 자바버전을 의미한다
repositories {
mavenCentral() 
//mavenCentral 사이트에서 자동으로 설정한 dependencies를 다운받아준다
}
dependencies {
implementation &#x27;org.springframework.boot:spring-boot-starter-thymeleaf&#x27;
implementation &#x27;org.springframework.boot:spring-boot-starter-web&#x27;
//설치해줬던 dependencies
testImplementation(&#x27;org.springframework.boot:spring-boot-starter-test&#x27;) {
exclude group: &#x27;org.junit.vintage&#x27;, module: &#x27;junit-vintage-engine&#x27;
/*자동으로 들어간 테스트 라이브러리 &#x27;junit 5번째 버전*/
}

}</code></pre><p id="16f4e3e1-6e4c-472f-a901-04f03f747ebc" class="">.gitignore : 자동으로 소스코드를 관리해주는 파일이다
@SpringBootApplication : 톰캣 웹서버가 내장되어 있어서 자체적으로 띄우면서 스프링부트가 같이올라온다</p><p id="bf54c45c-a53e-48bb-aaf1-971193d257fd" class="">settings --&gt; gradle 검색
Build and run using
Run tests using
둘 다 intellij idea 로 바꾸기 --&gt; gradle을 거치지 않고 바로 적용되어서 속도가 향상된다</p><p id="bd1f80c8-2031-4c10-af10-5982db86531e" class="">
</p><p id="8e778958-460c-453d-ad3c-b3c9f652a805" class=""><strong>1-2.라이브러리 살펴보기</strong>
External Libraries
gradle이나 maven같은 빌드툴들은 의존관계를 관리해 준다 dependencies에서 설치된 것들 중에서
필요로 하는 의존들을 자동으로 더 땡겨온다
요즘은 탐켓이 임베디드(내장)되어 있음
현업에서는 로그 출력이 필요하다</p><ul id="3732c09b-dd6e-497f-b0c1-7516f8b71b66" class="bulleted-list"><li>spring-boot-starter-logging
slf4j : 인터페이스
logback: slf4j 구현, 실제 로그를 어떤 구현체로 출력할 것인가</li></ul><p id="b085ede5-7bce-46a2-a846-c2f1fa8366d7" class="">junit: 자바에서 사용하는 유닛테스트</p><p id="911204a0-ccf7-49f0-86b5-b4677637db9c" class="">
</p><p id="672b6bad-faf0-454d-9096-2448564a68cf" class=""><strong>1-3.View 환경설정</strong>
-welcome page
static 파일(정적 파일)에서 index.html을 찾아서 실행한다
<a href="https://docs.spring.io/spring-boot/docs/2.3.12.RELEASE/reference/html/">https://docs.spring.io/spring-boot/docs/2.3.12.RELEASE/reference/html/</a>
페이지에서 필요한 것 찾아보기</p><p id="2b2a533a-4ae5-40af-b839-6fb5ee40058a" class="">Controller 처음 시작할때 실행된다
&lt;HelloController&gt;</p><pre id="4e619ddf-293d-42c9-9499-3499700d8b03" class="code"><code>@GetMapping(&quot;hello&quot;) 
//웹 어플리케이션에서 /hello라고 들어오면 이 메서드를 호출해 준다
//get,post 메서드</code></pre><p id="4db6f414-7678-4cb5-91ba-d828b33cdbaa" class="">&lt;hello.html&gt;</p><pre id="3fef59ba-79e8-42a8-9fb2-ad79b8400349" class="code"><code>&lt;p th:text=&quot;&#x27;안녕하세요. &#x27; + ${data}&quot; &gt;안녕하세요. 손님&lt;/p&gt;
&lt;!--th: thymeleaf 의미--&gt;</code></pre><pre id="f452634a-869c-43f3-aac5-3ee2e6374fe8" class="code"><code>//Controller
public class HelloController {
@GetMapping(&quot;hello&quot;)
public String hello(Model model) {
model.addAttribute(&quot;data&quot;, &quot;hello!!&quot;);
return &quot;hello&quot;;
}//hello.html을 찾는다
}</code></pre><p id="08e295ae-c941-437c-b584-36e3a80f19a8" class="">
</p><p id="864320d5-e71f-4a17-bcbd-e330d998beaf" class=""><strong>1-4&lt;빌드하고 실행하기&gt;</strong>
cmd창
F:\study\hello-spring\hello-spring 로 이동
gradlew clean build --info
cd build/libs  로 이동</p><p id="93289142-c0ed-4e6c-9a74-488557db4d41" class="">
</p><p id="52414e29-4101-42fb-a10f-90f12610befd" class="">
</p><h3 id="f1848e8c-b3ce-4fa1-b29a-36cd401b747e" class="">2.스프링 웹 개발 기초</h3><p id="130acef7-39f7-4085-af7f-589207ce76de" class=""><strong>2-1정적 컨텐츠</strong>:파일을 그대로 고객에게 전달해 주는 것</p><p id="deb62ca0-b25e-4f4d-9a7b-aa4734ac5328" class=""> --&gt; 스프링부트에서 자동으로 제공한다
컨트롤러에서 매핑된 것을 찿지 못한 다면 static 파일에서 파일을 찾아서 반환해 준다</p><p id="4a15536e-404d-46da-af10-7bbca3030844" class="">
</p><p id="bda1374a-a909-4411-a0b6-f0ac171e19a3" class=""><strong>2-2 MVC와 템플릿 엔진 </strong>: ex)jsp처럼  html을 동적으로 바꿔주는 것
model1방식 : view에 모두 작성해 주는 것
관심사 분류, 역할과 책임
view: 화면을 그리는데 모든 영향을 집중
model, controller: 비즈니스 로직과 관련 내부적인 것을 처리하는데 집중해야 한다</p><pre id="db608148-27e8-45ba-9b4b-ab6b1b6616d4" class="code"><code>model.addAttribute(&quot;data&quot;, &quot;hello!!&quot;); //data에 직접 이름을 넣어준다
@GetMapping(&quot;hello-mvc&quot;) //url에 띄울 이름
public String helloMvc(@RequestParam(&quot;name&quot;) String name, Model model){
//@RequestParam(&quot;name&quot;,  required = false) 설정해 주면 값을 넘기지 않아도 에러가 안난다
model.addAttribute(&quot;name&quot;, name);//name에 파라미터에서 받아온 이름을 넘긴다
return  &quot;hello-template&quot;; //전달할 html파일
}</code></pre><p id="9adcce2f-e890-408d-8944-d2eded08948e" class=""><a href="http://localhost:8080/hello-mvc?name=spring">http://localhost:8080/hello-mvc?name=spring</a>!!
viewResolver: 화면에 관련된 해결자
정적 소스는 변환과정이 없지만 템플릿 엔진은 변환과정이 존재함</p><p id="754f87fc-60fb-44ea-9a08-2fa7d23cbd0c" class="">
</p><p id="46bb841b-aab2-4127-b34a-72ffc51818af" class=""><strong>2-3. API</strong> : 데이터구조 포멧(json)으로 클라이언트에게 데이터를 전달하는 방식</p><p id="c3e1c918-1e47-4df9-8fcb-b459acaf9939" class="">ex) vue,react적용하거나 서버끼리 통신할때 많이 사용한다
@GetMapping(&quot;hello-string&quot;) //문자열 받기 예제
@ResponseBody
http body부분에 데이터를 직접 넣어 준다는 의미,
뷰를 만들 필요 없이 문자가 바로 적용된다
{&quot;name&quot;:&quot;spring!!&quot;} 키 값 구조
JSON</p><p id="828530cb-2b9c-434e-afd6-94caa565e9a9" class="">자바빈 표준 방식, property 접근 방식
Alt + Insert: getter,setter 단축키</p><p id="5328c27a-99d3-4436-8b07-5e024d8fdc76" class="">controller가 url을 템플릿 엔진에서 찾지만
@ResponseBody가 있는 경우 그대로 응답에 그대로 데이터를 던져 넣는다
객체인 경우에는 json방식으로 데이터를 만들어서 http에 응답을 함
json으로 바꿔주는 라이브러리: Jackson(스프링에서 기본), gson</p><p id="cde167fb-6d9e-4340-b7d0-43a900cf2fe4" class="">
</p><h3 id="0afa822b-26fd-4630-a95e-e8ba3ee70905" class="">3.회원 관리 예제 - 백엔드 개발</h3><p id="12043a37-0bc4-4074-b9dc-020ccd4516ed" class="">
<strong>3-1. 비즈니스 요구사항 정리</strong>
서비스: 핵심 비즈니스 로직 구현 예) 회원은 중복가입이 안된다 등등의 로직
비즈니스 도메인객체를 가지고 핵심 비즈니스 로직이 동작하도록 구현한 계층
리포지토리: 데이터베이스에 접근, 도메인 객체를 DB에 저장하고 관리
도메인: 비즈니스 도메인 객체,
예) 회원, 주문, 쿠폰 등등 주로 데이터베이스에 저장하고 관리</p><p id="1b5897d8-a0c6-4ee2-8981-5f50e11341ae" class="">아직 데이터 저장소가 선정되지 않아서, 우선 인터페이스로 구현 클래스를 변경할 수 있도록 설계
--&gt; 인터페이스로 만들어 놓으면 나중에 데이터베이스변경이 가능하다</p><p id="e7aebd78-974f-4d53-b8fd-d9a4ff706be2" class="">
</p><p id="1d7ca5c2-ddca-4f37-9671-d7097d173c34" class=""><strong>3-2회원 도메인과 리포지토리 만들기</strong></p><p id="5b03664f-9ca6-43ab-9ccf-9e7983462e51" class="">
</p><p id="9f445f6a-b8e0-4310-97ce-1efa1a88a4d6" class=""><strong>3-3회원 리포지토리 테스트 케이스 작성</strong>
테스트는 의존 관계없이 설계가 되어야 한다
--&gt; 순서에 영향을 받지 않게 해줘야 한다</p><p id="c3b460e1-59f7-4cf7-91ee-b43511a0ac6d" class="">
</p><p id="eb7b346b-b039-4158-b2e8-61923f04801a" class=""><strong>3-4회원 리포지토리 테스트 케이스 작성</strong>
실제 비즈니스 로직을 구현하는 법</p><p id="fff8dfad-db87-49b7-b075-de1e9883f416" class="">
</p><p id="e7a4fbb5-a089-431e-9888-51281d8327c9" class=""><strong>3-5회원 서비스 테스트</strong>
클래스명에 마우스 위치 후, alt + enter --&gt; 테스트 클래스 자동생성</p><pre id="193dbeef-83e2-4a92-beb6-4c03736c2644" class="code code-wrap"><code>package hello.hellospring.service;

import hello.hellospring.domain.Member;
import hello.hellospring.repository.MemoryMemberRepository;
import org.junit.jupiter.api.Assertions;
import org.junit.jupiter.api.Test;

import static org.assertj.core.api.Assertions.*;
import static org.junit.jupiter.api.Assertions.*;

class MemberServiceTest {
MemberService memberService;
MemoryMemberRepository memberRepository;
@Test
void 회원가입() {
    //Given: 어떤 데이터를 기반으로 하는지
    Member member = new Member();
    member.setName(&quot;hello&quot;);

    //when: 어떤것을 검증하는지
    Long saveId = memberService.join(member);

    //then
    Member findMember = memberRepository.findById(saveId).get();
    assertThat(member.getName()).isEqualTo(findMember.getName());

}

@Test
void findMembers() {
}

@Test
void findOne() {
}
</code></pre><p id="2823b3ad-8ae8-4785-81a8-4583a609cac5" class="">}</p><p id="765fa9c1-959f-4de1-8750-a4137ac51948" class="">
</p></div></article></body></html>
