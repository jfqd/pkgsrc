# $NetBSD: Makefile,v 1.6 2017/11/16 01:28:12 khorben Exp $

DISTNAME=	rhash-1.3.5
PKGREVISION=	1
CATEGORIES=	security
MASTER_SITES=	${MASTER_SITE_GITHUB:=rhash/}
GITHUB_PROJECT=	RHash
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/rhash/RHash
COMMENT=	Calculate/check CRC32, MD5, SHA1, GOST, TTH, BTIH or other hash sums
LICENSE=	mit

WRKSRC=			${WRKDIR}/${DISTNAME:S/rh/RH/}
INSTALLATION_DIRS=	bin include lib ${PKGMANDIR}/man1 share/examples/rhash

MAKE_FLAGS+=	ADDCFLAGS=${CFLAGS:Q}
MAKE_FLAGS+=	ADDLDFLAGS=${LDFLAGS:Q}

CONF_FILES+=		${PREFIX}/share/examples/rhash/rhashrc ${PKG_SYSCONFDIR}/rhashrc

do-install:
	cd ${WRKSRC} && \
	${INSTALL_PROGRAM} rhash ${DESTDIR}${PREFIX}/bin && \
	${INSTALL_LIB} librhash/librhash.a ${DESTDIR}${PREFIX}/lib && \
	${INSTALL_DATA} librhash/rhash.h librhash/rhash_timing.h ${DESTDIR}${PREFIX}/include && \
	${INSTALL_DATA} dist/rhash.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1 && \
	${INSTALL_DATA} dist/rhashrc.sample ${DESTDIR}${PREFIX}/share/examples/rhash/rhashrc

.include "../../security/openssl/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
