# $NetBSD: Makefile,v 1.10 2017/10/09 12:30:22 kleink Exp $

DISTNAME=	WeasyPrint-0.41
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:tl}
CATEGORIES=	print python
MASTER_SITES=	${MASTER_SITE_PYPI:=W/WeasyPrint/}

MAINTAINER=	kleink@NetBSD.org
HOMEPAGE=	http://weasyprint.org/
COMMENT=	Converts HTML/CSS documents to PDF
LICENSE=	modified-bsd

USE_LANGUAGES=	# empty

DEPENDS+=	pango-[0-9]*:../../devel/pango
DEPENDS+=	${PYPKGPREFIX}-cairosvg>=1.0.20:../../converters/py-cairosvg
DEPENDS+=	${PYPKGPREFIX}-cairocffi>=0.5:../../graphics/py-cairocffi
DEPENDS+=	${PYPKGPREFIX}-html5lib>=0.999999999:../../textproc/py-html5lib
DEPENDS+=	${PYPKGPREFIX}-pdfrw>=0.4:../../textproc/py-pdfrw
DEPENDS+=	${PYPKGPREFIX}-tinycss2>=0.5:../../textproc/py-tinycss2
DEPENDS+=	${PYPKGPREFIX}-cssselect2>=0.1:../../textproc/py-cssselect2
DEPENDS+=	${PYPKGPREFIX}-pyphen>=0.8:../../textproc/py-pyphen

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
