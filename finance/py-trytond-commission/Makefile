# $NetBSD: Makefile,v 1.2 2017/09/16 19:26:53 wiz Exp $
TRYTON_MODULE_NAME=	trytond_commission
.include "../../devel/py-trytond/Makefile.common"
CATEGORIES=	finance python

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.tryton.org/
COMMENT=	Commission module of the Tryton application platform
LICENSE=	gnu-gpl-v3

DEPENDS+=	${PYPKGPREFIX}-simpleeval-[0-9]*:../../math/py-simpleeval
DEPENDS+=	${PYPKGPREFIX}-python-sql-[0-9]*:../../databases/py-python-sql
DEPENDS+=	${PYPKGPREFIX}-trytond-account>=${TRYTON_BASEVER}:../../finance/py-trytond-account
DEPENDS+=	${PYPKGPREFIX}-trytond-account-invoice>=${TRYTON_BASEVER}:../../finance/py-trytond-account-invoice
DEPENDS+=	${PYPKGPREFIX}-trytond-account-product>=${TRYTON_BASEVER}:../../finance/py-trytond-account-product
DEPENDS+=	${PYPKGPREFIX}-trytond-party>=${TRYTON_BASEVER}:../../misc/py-trytond-party
DEPENDS+=	${PYPKGPREFIX}-trytond-product>=${TRYTON_BASEVER}:../../misc/py-trytond-product
DEPENDS+=	${PYPKGPREFIX}-trytond>=${TRYTON_BASEVER}:../../devel/py-trytond

USE_LANGUAGES=	# none

.include "../../lang/python/application.mk"
.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
