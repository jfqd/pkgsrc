# $NetBSD: Makefile,v 1.29 2017/09/23 20:34:11 wiedi Exp $

DISTNAME=	bing_src-1.1.3
PKGNAME=	${DISTNAME:S/_src//}
CATEGORIES=	net
MASTER_SITES=	http://fgouget.free.fr/bing/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://fgouget.free.fr/bing/index-en.shtml
COMMENT=	Bing is a point-to-point bandwidth measurement tool
LICENSE=	original-bsd

USE_TOOLS+=	groff
LDFLAGS.SunOS+=	-lsocket -lnsl

INSTALLATION_DIRS=	bin ${PKGMANDIR}/man8 share/doc/bing

post-install:
	${INSTALL_DATA} ${WRKSRC}/Readme.txt ${DESTDIR}${PREFIX}/share/doc/bing

.include "../../mk/bsd.pkg.mk"

# XXX On NetBSD the gcc-2.95.3 for:
# XXX
# XXX     alpha
# XXX
# XXX has an optimization bug when compiling with -O2 that is tickled by
# XXX ${WRKSRC}/bing.c
#
.if ${OPSYS} == "NetBSD"
.  if (${MACHINE_ARCH} == "alpha")
CXXFLAGS:=	${CXXFLAGS:C/-O[0-9]*//g}
CFLAGS:=	${CFLAGS:C/-O[0-9]*//g}
.  endif
.endif
