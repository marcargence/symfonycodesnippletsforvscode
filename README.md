# Symfony Code Snipplets for VSCode

#### twig.json

```json
{
	"Twig form row": {
		"prefix": "twformrow",
		"body": [
			"{{ form_row(form.$1) }}"
		],		
	},	
	"Twig form row full": {
		"prefix": "twformrowfull",
		"body": [
			"<div class=\"form-control\">",
			"\t{{ form_label(form.${1:FIELD}) }}",
			"\t{{ form_widget(form.${1:FIELD}) }}",
			"\t{{ form_errors(form.${1:FIELD}) }}",
			"</div>"
		],		
	},	
	"Twig asset": {
		"prefix": "twasset",
		"body": [
			"{{ asset('$1') }}"
		],		
	},		
	"Twig trans": {
		"prefix": "twtrans",
		"body": [
			"{{ '$1'|trans }}"
		],		
	},			
}
```

#### php.json
```json
{
	"Symfony repofind": {
		"prefix": "sfrepofind",
		"body": [
			"$this->getDoctrine()->getRepository('$1')->$2($3);"
		]		
	},	
	"Symfony get em": {
		"prefix": "sfem",
		"body": [
			"$em = $this->getDoctrine()->getManager();"
		]		
	},	
	"Symfony create query": {
		"prefix": "sfcreatequery",
		"body": [
			"$1 = $em->getRepository('$2')",
			"\t->createQueryBuilder('${3:ALIAS}')",
			"\t\tWHERE ${3:ALIAS}.${4:PROPERTY} = :${5:PARAMETER}')",
			"\t->setParameter('${5:PARAMETER}', ${6:ARGUMENT})",
			"\t->getQuery();"
		]	
	},	
	"Symfony rendertwig": {
		"prefix": "sfrendertwig",
		"body": [
			"return $this->render('$1', [$2]);"
		]
	},	
	"Symfony createaction": {
		"prefix": "sfact",
		"body": [
			"/**",
			"* @Route(\"/$1\", name=\"$2\")",
			"*/",
		   "public function $3Action()",
		   "{",
			"   $4",
		   "}"
		]
	},	
	"Symfony doctrine column": {
		"prefix": "ormcolumn",
		"body": [
			"/**",
			"* @ORM\\Column(type=\"$1\")",
			"*/",
		   "private $2;"
		]
	},
	"Symfony route": {
		"prefix": "sfroute",
		"body": [
			"/**",
			"* @Route(\"/$1\", name=\"$2\")",
			"*/"
		]
	},
	"Symfony form handle": {
		"prefix": "sfformhandle",
		"body": [
			"$form = $this->createForm($1::class);",
			"",
			"$form->handleRequest($request);",
			"if ($form->isSubmitted() && $form->isValid()) {",
			"",
			"$this->addFlash('success', '$2');",
			"",
			"return $this->redirectToRoute('$3', []);",
			"}",
		]
	},		

}
```
references:
https://github.com/knpuniversity/phpstorm-settings/blob/master/README.md
