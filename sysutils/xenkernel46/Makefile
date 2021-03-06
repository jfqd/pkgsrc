# $NetBSD: Makefile,v 1.17 2017/12/15 14:00:44 bouyer Exp $

VERSION=	4.6.6
DISTNAME=	xen-${VERSION}
PKGNAME=	xenkernel46-${VERSION}
PKGREVISION=	2
CATEGORIES=	sysutils
MASTER_SITES=	https://downloads.xenproject.org/release/xen/${VERSION}/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://xenproject.org/
COMMENT=	Xen 4.6.x Kernel

LICENSE=	gnu-gpl-v2

ONLY_FOR_PLATFORM=	Linux-2.6*-x86_64
ONLY_FOR_PLATFORM+=	NetBSD-[5-9].*-x86_64

PKGSRC_USE_SSP=	no

NO_CONFIGURE=	yes
USE_TOOLS+=	gmake

PYTHON_FOR_BUILD_ONLY=		YES
PYTHON_VERSIONS_INCOMPATIBLE=	34 35 36

MAKE_ENV+=	OCAML_TOOLS=no

INSTALLATION_DIRS=	xen46-kernel
XENKERNELDIR=		${PREFIX}/${INSTALLATION_DIRS}

MESSAGE_SUBST+=		XENKERNELDIR=${XENKERNELDIR}

.include "../../mk/compiler.mk"
.if !empty(PKGSRC_COMPILER:Mclang)
EXTRA_CFLAGS+=	-Qunused-arguments -no-integrated-as -Wno-error=format \
		-Wno-error=parentheses-equality -Wno-error=enum-conversion \
		-Wno-error=unused-function -Wno-error=unused-const-variable \
		-Wno-error=ignored-attributes -Wno-error=constant-conversion \
		-Wno-error=address-of-packed-member \
		-Wno-error=initializer-overrides \
		-Wno-error=tautological-compare
.endif

MAKE_ENV+=	EXTRA_CFLAGS=${EXTRA_CFLAGS:Q}

do-build:
	cd ${WRKSRC}/xen && ${BUILD_MAKE_CMD} debug=n build
	${CP} ${WRKSRC}/xen/xen.gz ${WRKDIR}/xen.gz
	cd ${WRKSRC}/xen && ${MAKE_PROGRAM} clean
	cd ${WRKSRC}/xen && ${BUILD_MAKE_CMD} debug=y build
	${CP} ${WRKSRC}/xen/xen.gz ${WRKDIR}/xen-debug.gz

do-install:
	${INSTALL_DATA} ${WRKDIR}/xen.gz \
	    ${DESTDIR}${XENKERNELDIR}/xen.gz
	${INSTALL_DATA} ${WRKDIR}/xen-debug.gz \
	    ${DESTDIR}${XENKERNELDIR}/xen-debug.gz

.include "../../lang/python/application.mk"
.include "../../mk/bsd.pkg.mk"
